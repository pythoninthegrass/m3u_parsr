# m3u_parser

Parses an M3U playlist file into a list of track objects.

Builds on the excellent work of [dvndrsn's](https://github.com/dvndrsn) [M3uParser](https://github.com/dvndrsn/M3uParser).

## Setup
* Minimum requirements
  * [Python 3.11](https://www.python.org/downloads/)
* Dev dependencies
  * [editorconfig](https://editorconfig.org/)

## Quickstart
```bash
# setup virtual environment
python -m venv .venv
source .venv/bin/activate

# install
python -m pip install m3u-parsr

# run
m3u-parser ./tests/fixtures/test.m3u
```

## Development
* Testing
    ```
    # activate virtual environment
    poetry shell

    # run against the example m3u file
    λ app/main.py ./tests/fixtures/test.m3u
    Minus The Bear - Burying Luck.mp3 (0s)
    Minus The Bear - Ice Monster.mp3 (0s)
    Minus The Bear - Knights.mp3 (0s)
    Minus The Bear - White Mystery.mp3 (0s)
    Minus The Bear - Dr. l'Ling.mp3 (0s)
    Minus The Bear - Part 2.mp3 (0s)
    Minus The Bear - Throwin' Shapes.mp3 (0s)
    Minus The Bear - When We Escape.mp3 (0s)
    Minus The Bear - Double Vision Quest.mp3 (0s)
    Minus The Bear - Lotus.mp3 (0s)
    Parsed 10 tracks from ../tests/fixtures/test.m3u
    
    # generate tests
    cd app/
    hypothesis write m3u_parser.parsem3u > ../tests/test_m3u_parser.py

    # run specific test
    pytest -k test_m3u_parser

    # install from testpypi
    pip install -i https://test.pypi.org/simple/ m3u-parsr
    ```

## TODO
* [Issues](https://github.com/pythoninthegrass/m3u_parser/issues)
* Button up error handling for internal field separators on m3u track names
* Tests
* CI/CD

## Further Reading
[The M3U File Format « The Matthew Nielsen Web Experience](https://web.archive.org/web/20180809050707/http://n4k3d.com/the-m3u-file-format)

[Repositories | Documentation | Poetry - Python dependency management and packaging made easy](https://python-poetry.org/docs/repositories/)

[How to Build and Publish Python Packages With Poetry](https://www.freecodecamp.org/news/how-to-build-and-publish-python-packages-with-poetry/)

[`poetry publish` raises HTTP 403 · Issue #6320 · python-poetry/poetry](https://github.com/python-poetry/poetry/issues/6320#issuecomment-1234036608)
