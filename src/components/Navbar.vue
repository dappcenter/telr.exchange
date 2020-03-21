<template>
    <nav class="navbar navbar-light bg-light navbar-expand-lg">
        <a class="navbar-brand text-primary" href="/">
            Telr<span class="text-info">Exchange</span>
        </a>

        <button class="navbar-toggler" type="button" data-toggle="collapse" data-target="#navbarNav" aria-controls="navbarNav" aria-expanded="false" aria-label="Toggle navigation">
            <span class="navbar-toggler-icon"></span>
        </button>

        <div class="collapse navbar-collapse" id="navbarNav">
            <ul class="navbar-nav mr-auto">
                <li class="nav-divider"></li>

                <li class="theme-selector nav-item">
                    <a class="nav-link" href="javascript://" onclick="document.querySelector('body').classList.remove('light'); document.querySelector('body').classList.add('dark');">
                        <i class="fa fa-square" aria-hidden="true"></i>
                    </a>

                    <a class="nav-link" href="javascript://" onclick="document.querySelector('body').classList.remove('dark'); document.querySelector('body').classList.add('light');">
                        <i class="far fa-square" aria-hidden="true"></i>
                    </a>
                </li>

                <li class="nav-divider"></li>

                <li class="nav-item dropdown" id="tokensDropdown">
                    <a href="javascript://" class="nav-link dropdown-toggle" data-toggle="dropdown" role="button" aria-haspopup="true" aria-expanded="false">
                        Bai Stablecoin (BAI)&nbsp;
                    </a>

                    <ul class="dropdown-menu">
                        <li>
                            <form>
                                <input type="search" class="form-control" id="searchToken" placeholder="Search coins &amp; tokens">
                            </form>
                        </li>

                        <!-- separator -->
                        <li role="separator" class="dropdown-divider"></li>

                        <li>
                            <h5 class="text-center text-info">Featured Tokens</h5>
                        </li>

                        <li class="dropdown-item btn text-primary">
                            Bai Stablecoin <small><small class="text-muted">[ <span class="text-primary">BAI</span> ]</small></small>
                        </li>

                        <li class="dropdown-item btn text-primary">
                            Dai Stablecoin <small><small class="text-muted">[ <span class="text-primary">DAI</span> ]</small></small>
                        </li>

                        <li class="dropdown-item btn text-primary">
                            Spice <small><small class="text-muted">[ <span class="text-primary">SPICE</span> ]</small></small>
                        </li>

                        <!-- separator -->
                        <li role="separator" class="dropdown-divider"></li>

                        <li>
                            <h5 class="text-center text-info">Featured Coins</h5>
                        </li>

                        <li class="dropdown-item btn text-primary">
                            Bitcoin Cash <small><small class="text-muted">[ <span class="text-primary">BCH</span> ]</small></small>
                        </li>

                        <li class="dropdown-item btn text-primary">
                            Bitcoin Legacy <small><small class="text-muted">[ <span class="text-primary">BTC</span> ]</small></small>
                        </li>

                        <li class="dropdown-item btn text-primary">
                            Ethereum <small><small class="text-muted">[ <span class="text-primary">ETH</span> ]</small></small>
                        </li>

                        <!-- separator -->
                        <li role="separator" class="dropdown-divider"></li>

                        <li class="dropdown-item btn text-primary text-center" data-toggle="modal" data-target="#exampleModal">
                            Load more coins &amp; tokens...
                        </li>

                        <li class="dropdown-item btn text-primary text-center">
                            Add a custom token?
                        </li>
                    </ul>
                </li>
            </ul>

            <ul class="nav navbar-nav navbar-right">
                <li class="nav-item dropdown">
                    <a href="javascript://" class="nav-link" data-toggle="dropdown" role="button" aria-haspopup="true" aria-expanded="false">
                        <i class="far fa-user-circle"></i> <span>My Account</span></a>

                    <ul class="dropdown-menu dropdown-menu-right">
                        <li class="active dropdown-item"><a href="javascript://">{{profileAddress}}&nbsp;<span class="badge badge-dark">0.013 BCH</span>&nbsp;<span class="badge badge-success">MetaMask</span></a></li>
                        <li role="separator" class="dropdown-divider"></li>
                        <li class="dropdown-item btn text-info"><i class="fa fa-fw fa-piggy-bank"></i> Deposit <small><small class="text-danger">(Telr Wallet)</small></small></li>
                        <li class="dropdown-item btn text-info"><i class="fa fa-fw fa-money-check-alt"></i> Withdraw <small><small class="text-danger">(Telr Wallet)</small></small></li>
                        <li class="dropdown-item btn text-info" @click="signTrade"><i class="fa fa-fw fa-plug"></i> Sign Telr <small><small class="text-danger">(Telr DEX)</small></small></li>
                        <li class="dropdown-item btn text-info" @click="connectMetamask"><i class="fa fa-fw fa-plug"></i> Connect Metamask <small><small class="text-danger">(Web Wallet)</small></small></li>
                        <li class="dropdown-item btn text-info"><i class="fa fa-fw fa-plug"></i> Connect Ledger Nano S <small><small class="text-danger">(Hardware Wallet)</small></small></li>
                        <li class="dropdown-item btn text-info"><i class="fa fa-fw fa-plug"></i> Connect Trezor <small><small class="text-danger">(Hardware Wallet)</small></small></li>
                    </ul>
                </li>

                <li class="nav-item">
                    <a href="javascript://" class="nav-link text-primary" data-toggle="dropdown" role="button" aria-haspopup="true" aria-expanded="false">
                        <i class="fa fa-external-link-alt"></i> <span>Token Info</span></a>
                </li>

                <li class="nav-item dropdown">
                    <a href="javascript://" class="nav-link" data-toggle="dropdown" role="button" aria-haspopup="true" aria-expanded="false">
                        <i class="fa fa-language"></i> English
                    </a>

                    <ul class="dropdown-menu dropdown-menu-right">
                        <li class="dropdown-item"><a href="javascript://"><span>English</span></a></li>
                        <li class="dropdown-item"><span class="text-muted">中文</span></li>
                        <li class="dropdown-item"><span class="text-muted">Español</span></li>
                        <li class="dropdown-item"><span class="text-muted">한국어</span></li>
                        <li class="dropdown-item"><span class="text-muted">русский</span></li>
                    </ul>
                </li>

                <li class="nav-item dropdown">
                    <a href="javascript://" class="nav-link text-danger" data-toggle="dropdown" role="button" aria-haspopup="true" data-offset="50,50" aria-expanded="false">
                        <i class="far fa-life-ring"></i>&nbsp;<span>Need Help?</span>
                    </a>
                    <ul class="dropdown-menu dropdown-menu-right">
                        <li class="dropdown-item"><a href="http://riot.im/app" target="_blank"><i class="far fa-fw fa-comment" aria-hidden="true"></i> <span>[ Matrix ]</span></a></li>
                        <li class="dropdown-item"><a href="https://www.reddit.com/r/TelrExchange" target="_blank"><i class="fab fa-fw fa-reddit-alien" aria-hidden="true"></i> Reddit</a></li>
                        <li class="dropdown-item">
                            <a href="https://ropsten.etherscan.io/address/#code" target="_blank">
                                <i class="far fa-fw fa-file-alt" aria-hidden="true"></i>
                                Contract 0xEb3D8484D7..
                                <small class="text-success">(Latest 2019.03.12)</small>
                            </a>
                        </li>
                    </ul>
                </li>
            </ul>
        </div>

        <!-- Modal -->
        <div class="modal fade" id="exampleModal" tabindex="-1" role="dialog" aria-labelledby="exampleModalLabel" aria-hidden="true">
            <div class="modal-dialog" role="document">
                <div class="modal-content">
                    <div class="modal-header">
                        <h5 class="modal-title" id="exampleModalLabel">Modal title</h5>
                        <button type="button" class="close" data-dismiss="modal" aria-label="Close">
                            <span aria-hidden="true">&times;</span>
                        </button>
                    </div>

                    <div class="modal-body">
                        ...
                    </div>

                    <div class="modal-footer">
                        <button type="button" class="btn btn-secondary" data-dismiss="modal">Close</button>
                        <button type="button" class="btn btn-primary">Save changes</button>
                    </div>
                </div>
            </div>
        </div>
    </nav>
</template>

<script>
/* Initialize vuex. */
import { mapActions, mapGetters, mapState } from 'vuex'

export default {
    props: {
        // msg: String
    },
    computed: {
        ...mapState({
            profileAddress: state => state.profileAddress,
        }),

        ...mapGetters({
            //
        }),
    },
    methods: {
        ...mapActions({
            //
        }),

        connectMetamask() {
            console.log('TODO: connect metamast')
        },

        signTrade() {
            console.log('TODO: sign trade')
        },

    },
    created: function () {
        //
    },
    mounted: function () {
        //
    },
}
</script>

<style scoped>
/*  */
</style>
