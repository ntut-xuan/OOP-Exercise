# Encapsulation

## Why we need encapsulation?

We provide some function to change the state of laptop. For example, change the brightness, change the computer name...

But consider these situation:

- How about change the Model of CPU?
- How about change the brightness into 48763%? The value is over than 100%, how it possible?

It's impossible to change the CPU when the laptop is constructed. Moreover, it also impossible to change the brightness over than 100%.

<img src="../assets/Unreasonable-CPU-setup.png" alt="Computer" style="zoom: 75%;" />

But if it's possible that user can change any state, the user may change the CPU model, the user may change the brightness into 48763% also. These operation is violated our policy.

The reason why need Encapsulation is prevent user change the state directly. If user want to change the state, it should change through the function.

## What's encapsulation?

The encapsulation in OOP is preventing user changing the state directly.

For example, if we trying to perform these operations:

| Operations                                             | Is it OK? | Reason                                                     |
| ------------------------------------------------------ | :-------: | ---------------------------------------------------------- |
| Trying to change the brightness into 45%               |    OK     | You can change the brightness of the laptop into 45%.      |
| Trying to change the laptop name into "It's my laptop" |    OK     | You can change the laptop name with any non-empty name.    |
| Trying to change the CPU Model                         |    NO     | You can't change the CPU model when laptop is constructed. |
| Trying to change the brightness into 48763%            |    NO     | The brightness should between 0% to 100%.                  |

There have some possible operation that is not OK to perform. If user can change the state directly, these operations may be performed.

So, we need encapsulation to prevent the state can change by user directly. Instead, we provide some function to user, and hide the member (which is, state) to user. The user only change the state by function, instead of change the state directly. With using function to change the state, it can have some checking to make sure the state user want to replace is fulfilled condition and prevent abnormal situation happened.

In the example we provide, the user only can change brightness with `SetBrightness()` function and change name with `SetName()` function. Since it's impossible to change CPU Model, we won't provide any function to change the CPU Model. In addition, the functions should have some condition to check the state is fulfilled. For example, `SetBrightness()` function should check the brightness value is between 0% to 100%. Moreover, the user can not change the state directly since the member (which is, state) is hidden for user.

With Encapsulation, we can make sure that the state not to be changed from user directly. With some checking, it's kind a protection for object that prevent any abnormal state appeared in object and caused some disaster.

In the next section, we will try to describe how to do Encapsulation.

## How to do encapsulation?

Since Encapsulation prevent user change the state directly, we provide some function to let user interactive with object, instead let user access the state directly.

In the example we provide above, we have `SetBrightness()` function to change brightness, and `SetName()` function to change name. The user can change the state by these function.

When we provide these function, we can perform these checking also:

- When user trying to change the brightness, should check the brightness should between 0% to 100%. Otherwise, should throw exception when the state is not fulfilled.
- When user trying to change the name, should check the name should be non-empty. Otherwise, should throw exception when the state is not fulfilled.

<img src="../assets/Encapsulation-on-method.png" alt="Computer" style="zoom: 75%;" />

Encapsulation make sure the user can't change the state directly. Instead, encapsulation provide some function for user to change the state. It noteworthy that good encapsulation should consider the user may input some abnormal state into function and prevent these state changed into the object and cause some abnormal situtation happened.
