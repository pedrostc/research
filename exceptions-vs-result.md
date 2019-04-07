# References

## Articles

- [01 - Error Handling — Returning Results](https://medium.com/@michael_altmann/error-handling-returning-results-2b88b5ea11e9)
- [02 - Fowler - Notifications](https://martinfowler.com/eaaDev/Notification.html)
- :star2: [03 - Fowler - Replacing Throwing Exceptions with Notification in Validations](https://martinfowler.com/articles/replaceThrowWithNotification.html)
> - Exceptions signal something outside the expected bounds of behavior of the code in question. But if you're running some checks on outside input, this is because you expect some messages to fail - and if a failure is expected behavior, then you shouldn't be using exceptions.
> - We believe that exceptions should rarely be used as part of a program's normal flow: exceptions should be reserved for unexpected events. Assume that an uncaught exception will terminate your program and ask yourself, "Will this code still run if I remove all the exception handlers?" If the answer is "no", then maybe exceptions are being used in nonexceptional circumstances. -- Dave Thomas and Andy Hunt
- :star2: [04 - Khorikov - Error handling: Exception or Result?](https://enterprisecraftsmanship.com/2017/03/13/error-handling-exception-or-result/)
> - [Comments] In other words, if you as a library author don't know what to do with some failure, wrap it with your own exception and let it propagate further. For the client, the same failure might be an expected one so they can decide to convert it into a Result instance on their end.
> - Failures You don't know how to deal with - Also apply to failures that don't allow you go any further with you process, you can't do anything else if it happens, just fail.
> - [Summary] It’s pretty easy to differentiate use cases for Result and exceptions. Whenever the failure is something you expect and know how to deal with – catch it at the lowest level possible and convert into a Result instance. If you don’t know how to deal with it – let it propagate and interrupt the current business operation. Don’t catch exceptions you don’t know what to do about.
- [05 - Khorikov - Exceptions for flow control in C#](https://enterprisecraftsmanship.com/2015/02/26/exceptions-for-flow-control-in-c/)
> - Generally, code is read more often than written. Most of the best practices aimed to simplify understanding and reasoning about the code: the simpler code, the fewer bugs it contains, and the easier it becomes to maintain the software.
> - Examples of exceptional situations may include database connectivity problems, lack of required configuration files and so on. Validation is no such a situation because validation logic, by its definition, expects incoming data to be incorrect
> - Another valid use case for exceptions is code contract violation.
> - On the other hand, the developer who uses the library might expect that the database goes off-line from time to time and design their application for database failure.
> -  you shouldn’t wrap such code with a generic exception handler. Generic exception handler basically states that you expect any exceptions that could possibly be thrown.
> - You can put one at the topmost level to catch all exceptions that were not handled by your code in order to log them.
> - The best way to deal with unexpected exceptions is to discard the current operation completely.
- [06 - Khorikov - What is an exceptional situation in code?](https://enterprisecraftsmanship.com/2017/03/30/what-is-an-exceptional-situation-in-code/)
- [07 - Java - How to represent the result of an operation](https://codereview.stackexchange.com/questions/20285/java-how-to-represent-the-result-of-an-operation)
- [08 - Why catch(Exception)/empty catch is bad](https://devblogs.microsoft.com/dotnet/why-catchexceptionempty-catch-is-bad/)
- [09 - How to Deal With Exceptions](https://dzone.com/articles/how-to-deal-with-exceptions)
- [10 - Best practices for exceptions](https://docs.microsoft.com/en-us/dotnet/standard/exceptions/best-practices-for-exceptions)
- [11 - How expensive are exceptions in C#?](https://stackoverflow.com/questions/891217/how-expensive-are-exceptions-in-c)
- [12 - Skeet - Exceptions and Performance in .NET](https://www.developerfusion.com/article/5250/exceptions-and-performance-in-net/)
- [13 - Skeet - Exceptions and Performance Redux](https://web.archive.org/web/20190119001938/http://yoda.arachsys.com/csharp/exceptions2.html)
- [14 - The True Cost of .NET Exceptions — Solution](https://blogs.msdn.microsoft.com/ricom/2006/09/25/the-true-cost-of-net-exceptions-solution/)
- [15 - Cwalina - Design Guidelines Update: Exception Throwing](https://blogs.msdn.microsoft.com/kcwalina/2005/03/16/design-guidelines-update-exception-throwing/)
- [16 - Which part of throwing an Exception is expensive?](https://stackoverflow.com/questions/36343209/which-part-of-throwing-an-exception-is-expensive)
- [17 - Warren - Why Exceptions should be Exceptional](https://mattwarren.org/2016/12/20/Why-Exceptions-should-be-Exceptional/)
- [18 - The Exception Penalty In C#](https://mdfarragher.com/2017/11/08/the-exception-penalty-in-csharp/)
- [19 - The Cost of an Exception](https://www.dynatrace.com/news/blog/the-cost-of-an-exception/)
- [20 - Reinventing the Try/Catch Block](http://ryanmorr.com/reinventing-the-try-catch-block/)
- [21 - Joel - Exceptions](https://www.joelonsoftware.com/2003/10/13/13/)
- [22 - Wading In...](http://williamcaputo.com/posts/000009.html)
- [23 - C2 - You Dont Want An Exception You Wanta Time Machine](http://wiki.c2.com/?YouDontWantAnExceptionYouWantaTimeMachine)
- [24 - Java Exception Handling](http://neverworkintheory.org/2016/04/26/java-exception-handling.html)
- [25 - Feathers - Unconditional Code](https://www.youtube.com/watch?v=AnZ0uTOerUI)
- [26 - Feathers - Beyond Error Handling](https://vimeo.com/99668845)
- [27 - Sneaky exceptions](https://codejargon.blogspot.com/2015/02/sneaky-exceptions.html?m=1)
- [28 - Feathers - A Monadic Approach to Error Handling in Collection Pipelines](https://michaelfeathers.silvrback.com/a-monadic-approach-to-error-handling-in-collection-pipelines)
- [29 - Java - The exceptions debate](https://www.ibm.com/developerworks/java/library/j-jtp05254/index.html)
- [30 - Podcast - Feathers - Michael Feathers - First Class Error Handling, Tell Don't Ask, and Collection Pipelines](http://www.fullstackradio.com/39)
- [31 - Podcast - Clean Code – Error Handling](https://www.codingblocks.net/podcast/clean-code-error-handling/)
- [32 - Feathers - Abstracting Away From Exceptions](https://mjtsai.com/blog/2009/01/06/abstracting-away-from-exceptions/)
- [33 - Fail Fast](https://www.martinfowler.com/ieeeSoftware/failFast.pdf)
- [34 - Don't Overuse Exceptions](https://dalibornasevic.com/posts/52-don-t-overuse-exceptions)
- [35 - C2 - Don't use exceptions for flow control](http://wiki.c2.com/?DontUseExceptionsForFlowControl)
- [36 - SO - Why not use exceptions as regular flow of control](https://stackoverflow.com/questions/729379/why-not-use-exceptions-as-regular-flow-of-control)

## Code

- [FluentResults](https://github.com/altmann/FluentResults)