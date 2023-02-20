# Reservations API

## Local setup

Assuming you are using `rbenv` to manage your Ruby versions:

```
rbenv install 3.2.0
```

Clone the repo:

```
git clone --branch reservations-endpoint https://github.com/darrenpangan/reservations_api.git
```

Change to the project directory then install the gems:

```
cd reservations_api
bundle install
```

Run the tests:

```
bundle exec rspec spec
```

Run the local server at http://localhost:3000

```
bundle exec rails s
```

## Usage

The simplest way to test this is by using an API platform such as [Postman](https://www.postman.com/downloads/).

- Select `POST` as the method.
- Use `http://localhost:3000/reservations/create` as the action url.
- Under the "Body" tab, check "raw" and select "JSON" from the dropdown.
- Copy and paste the payload (JSON format) in the corresponding field.
- Click the "Send" button.

## Notes
- Some information in the payload that can be calculated were not included in the models (guest and reservation). For example, the total number of guests is present in the payloads. This can be calculated by adding the number of adult, children, and infant guests.

## To do's
- Validate that reservation start date is not ahead of end date.
- Add authorization.
- Creat GitHub actions that will run the tests on pull requests.