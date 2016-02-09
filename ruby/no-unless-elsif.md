# Ruby Does Not Have Unless/Elsif

I really do not like using `else` with `unless` but it is possible:

```
unless foo?
	# bar that thing
else
	# foo that thing even though we are using way too much brain power to figure out what is going on here
end
```

However, you cannot do this:

```
unless foo?
	# bar that thing
elsif bar?
	# baz that thing (brains...)
else
 	# foo that thing
end
```

[source](http://www.railstips.org/blog/archives/2008/12/01/unless-the-abused-ruby-conditional/)