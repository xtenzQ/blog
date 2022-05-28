---
title: About
icon: fas fa-info-circle
order: 4
---

> Add Markdown syntax content to file `_tabs/about.md`{: .filepath } and it will show up on this page.
{: .prompt-tip }

> Add Markdown syntax content to file `_tabs/about.md`{: .filepath } and it will show up on this page.
{: .prompt-info }

```java
public void step() throws OutputException {
    String inputLine = inputSystem.input();
    logger.info("Input command : " + inputLine);
    Processor processor = new Processor(this);
    try {
        processor.process(inputLine);
    } catch (InvalidCommandException | NoSuchElementException e) {
        outputSystem.sendError();
        logger.error(e);
    } catch (Exception e) {
        e.printStackTrace();
        logger.error(e);
    }
}
```
