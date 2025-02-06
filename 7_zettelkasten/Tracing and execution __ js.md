# Meta
2025-02-01 09:35
**Tags:** [[JavaScript]]
**Activity:** #learning 
**Status:** #completed 

# Tracing the execution
There are several buttons for it at the top of the right panel.

1. **Resume**
	- *Role:* continue the execution.
	- *Hotkey:* `F8`.
	- *Description:* Resumes the execution. If there are no additional breakpoints, then the execution just continues and the debugger loses control.
2. **Step**
	- *Role:* run the next command.
	- *Hotkey:* `F9`.
3. **Step over**
	- *Role:* run the next command, but *don’t go into a function*.
	- *Hotkey:* `F10`.
	- *Description*: Similar to “Step”, but behaves differently if the next statement is a function call (not a built-in, like `alert`, but a function of our own). “Step” gets into a nested function call and pauses the execution at its first line, while “Step over” executes the nested function call invisibly to us, skipping the function internals. The execution is then paused immediately after the function call.
4. **Step into**
	- *Role:* similar to “Step”, but behaves differently in case of asynchronous function calls. “Step” ignores async actions, such as `setTimeout` (scheduled function call), that execute later. The “Step into” goes into their code, waiting for them if necessary.
	- *Hotkey:* `F11`.
5. **Step out**
	- *Role:* continue the execution till the end of the current function.
	- *Hotkey:* `Shift+F11`.
	- *Description:* Continue the execution and stop it at the very last line of the current function. Handy when we accidentally entered a nested call using “Step”, but it doesn’t interest us, and we want to continue to its end as soon as possible.
6. **Enable/disable all breakpoints**
	- Doesn’t move the execution. Just a mass on/off for breakpoints.
7. **Enable/disable automatic pause in case of an error.**
	- When enabled, if the developer tools is open, an error during the script execution automatically pauses it. Then we can analyse variables in the debugger to see what went wrong. So if our script dies with an error, we can open the debugger, enable this option and reload the page to see where it dies and what’s the context at that moment.