## Environment checking

Jianzheng uses a lot of packages such as [OpenCV](https://github.com/opencv/opencv) and so on. Some special packages require special environment, like "only ASCII code in path". So, to make sure the code can run successfully, check the environment at first is a good way.

To do this, I defined a function named `setup`. I got inspiration from [Pygame](https://github.com/pygame/pygame). 

### Example

```python
import jianzheng
jianzheng.setup()
```

It will check all the requirements and if no problem it will print some text like:

```text
Welcome to use jianzheng 1.1.0!
```

### Errors might raise

#### Invalid Environment Path

```text
jianzheng.base.exceptions.InvalidEnvironmentPath: Environment absolute path does't allowed to have characters out of ASCII printable characters(decimal 32 ~ 126). (Current: ~/όραμα)
```

This is caused by your environment absolute path has some characters out of the [ASCII printable characters](http://facweb.cs.depaul.edu/sjost/it212/documents/ascii-pr.htm). Rename the folders then this problem will be solved.
