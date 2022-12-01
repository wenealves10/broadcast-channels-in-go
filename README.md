# broadcast-channels-in-go

# install the repository

`git clone https://github.com/wenealves10/broadcast-channels-in-go.git`<br>
`cd broadcast-channels-in-go`<br>
`go run *.go`

# The Project about the broadcast channels in go

### Conclusion and key takeaways

<p>
We can only read the same data from a channel once in Golang, in a way that it does not broadcast messages by default.
</p>

<p>The broadcast server works as a local version of client-server communication, it handles different requests such as: adding or removing a channel from the listeners’ slice.</p>

<p>This behavior was achieved by using a for-select structure with a graceful shutdown option, allowing us to close the listeners in the case where we no longer need the broadcast anymore.</p>

<p>This pattern exposes a public interface with only two methods: Subscribe and CancelSubscription. We could create different broadcasters that handle other kinds of business logic.</p>
