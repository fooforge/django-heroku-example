# Django example-app with PlanetScale on Heroku

This is an example Django app with its database hosted on PlanetScale and deployed to Heroku.

Note: I know there's credentials in the `settings.py`. They're just dummy credentials so don't waste your time. ;-)

## Deployment steps

```
heroku create
heroku buildpacks:set heroku/python
heroku config:set DISABLE_COLLECTSTATIC=1
git push --set upstream heroku main
git push heroku main
heroku ps:scale web=1
heroku open

# browse to /products and that'll list two products stored in a database hosted on PlanetScale
```
