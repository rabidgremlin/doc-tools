# doc-tools
Docker image filled with handy markdown and doc tools.

Contains:
* pandoc
* tex-live
* python
* git

**Note:** This is a large image since it contains the full text-live package.

## Example Usage

1. Create test directory
```
mkdir ~/doc-tools-test
```

2. Create a test markdown file `test.md` in `~/doc-tools-test` containing some markdown:
```
# Test markdown
This is some _test_ markdown.
```

3. Turn the markdown into a pdf
```
docker run --rm -v ~/doc-tools-test:/doc-tools-test rabidgremlin/doc-tools pandoc /doc-tools-test/test.md -o /doc-tools-test/te
st.pdf
```
