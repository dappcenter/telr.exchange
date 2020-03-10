<template>
    <div class="component">
        <div class="component-header text-warning"><span>Notices</span></div>

        <div class="component-tabs nav-header">
            <ul class="nav" role="tablist">
                <li role="presentation" class="nav-item">
                    <a href="javascript://" aria-controls="info" role="tab" data-toggle="tab" class="active nav-link" data-original-title="" title="">Important</a>
                </li>

                <li role="presentation" class="nav-item">
                    <a href="javascript://" aria-controls="twitter" role="tab" data-toggle="tab" class="nav-link" data-original-title="" title="">Reddit</a>
                </li>

                <li role="presentation" class="nav-item">
                    <a href="javascript://" aria-controls="twitter" role="tab" data-toggle="tab" class="nav-link" data-original-title="" title="">Read.cash</a>
                </li>
            </ul>
        </div>

        <div class="tab-content">
            <div role="tabpanel" class="tab-pane active" id="important">
                <div>
                    <p class="text-danger">IMPORTANT — PLEASE READ</p>

                    <p>
                        The only official URL for TelrExchange is:
                        <br />&nbsp;&nbsp;&nbsp;&nbsp; <strong class="text-primary">https://telr.exchange</strong>
                        <br />Bookmark it once and use the bookmark.
                    </p>

                    <p>
                        Do not send your tokens directly to the smart contract, or they will be lost and unrecoverable.
                        Use the Deposit form (upper-left) to send the proper deposit transaction.
                    </p>

                    <p>
                        The only official representative in the chat room is <strong>Modenero Support.</strong>
                    </p>

                    <p class="text-danger">Disclaimer</p>

                    <p>
                        TelrExchange is a decentralized trading platform that lets you trade multiple cryptocurrencies.
                    </p>

                    <p>
                        You are responsible for your own account, funds, and private keys.
                    </p>

                    <p>
                        You are responsible for your own trading decisions, and the details and mechanics of the tokens you trade.
                    </p>

                    <p>
                        TelrExchange is not responsible for your decisions, actions, or losses that result from using TelrExchange.
                    </p>

                    <p>
                        TelrExchange makes no guarantee about the tokens that you trade using TelrExchange.
                    </p>

                    <p>
                        TelrExchange does not hold your funds and does not offer refunds.
                    </p>

                    <p>
                        While the information contained on TelrExchange is periodically updated, no guarantee is given that the information provided on TelrExchange is correct, complete, or up-to-date.
                    </p>

                    <p>
                        By using TelrExchange, you acknowledge this and agree to these terms.
                    </p>
                </div>
            </div>
        </div> <!-- tab-content -->
    </div> <!-- component -->
</template>

<script>
export default {
    props: {
        // msg: String
    }
}
</script>

<style scoped>
/*  */
</style>
