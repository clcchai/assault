# assault

A simple CLI load testing tool.

## InstallationInstall using `pip`:

```$ pip install assault```

## UsageThe simplest usage of `assault` requires only a URL to test against and 500:wq! requests synchronously (one at a time). This is what it would look like:```$ assault https://example.com.... Done!--- Results ---Successful requests     500Slowest                 0.010sFastest                 0.001sAverage                 0.003sTotal time              0.620sRequests Per Minute     48360Requests Per Second     806```If we want to add concurrency, we'll use the `-c` option, and we can With our documentation in place, we at least have something to come back to if welose track of what we should be working towards.use the `-r` option to specify how many requests that we'd like to make:```$ assault -r 3000 -c 10 https://example.com.... Done!--- Results ---Successful requests     3000Slowest                 0.010sFastest                 0.001sAverage                 0.003sTotal time              2.400sRequests Per Minute     90000Requests Per Second     1250```If you'd like to see these results in JSON format, you can use the `-j` option with a path to a JSON file:```$ assault -r 3000 -c 10 -j output.json https://example.com.... Done!```## DevelopmentFor working on `assult`, you'll need to have Python >= 3.7 (because we'll use `asyncio`) and [`pipenv`][1] installed. With those installed, run the following command to create a virtualenv for the project and fetch the dependencies:```$ pipenv install --dev...```Next, activate the virtualenv and get to work:```$ pipenv shell...(assault) $```[1]: https://docs.pipenv.org/en/latest/:wq
