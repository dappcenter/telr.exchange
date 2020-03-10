<template>
    <div class="component">
        <div class="component-header text-warning">Buy / Sell</div>

        <div class="component-tabs nav-header">
            <ul class="nav" role="tablist">
                <li class="nav-item">
                    <a role="tab" data-toggle="tab" href="#buy" class="active nav-link" aria-controls="buy" aria-selected="true">Buy Order</a>
                </li>

                <li class="nav-item">
                    <a role="tab" data-toggle="tab" href="#sell" class="nav-link" aria-controls="sell" aria-selected="false">Sell Order</a>
                </li>
            </ul>
        </div>

        <div class="tab-content">
            <div role="tabpanel" class="tab-pane fade show active" id="buy">
                <form>
                    <div class="form-group">
                        <label for="buyAmount">Amount to buy</label>
                        <div class="input-group">
                            <input type="text" class="form-control form-control-sm" id="buyAmount">
                            <div class="input-group-append">
                                <span class="input-group-text">BAI</span>
                            </div>
                        </div>
                    </div>

                    <div class="form-group">
                        <label for="buyPrice">Price</label>
                        <div class="input-group">
                            <input type="text" class="form-control form-control-sm" id="buyPrice">
                            <div class="input-group-append">
                                <span class="input-group-text">BCH</span>
                            </div>
                        </div>
                    </div>

                    <div class="form-group">
                        <label for="buyTotal">Total</label>
                        <input type="text" id="buyTotal" class="form-control form-control-sm" value="" readonly="">
                    </div>

                    <div class="form-group">
                        <label for="buyExpires" data-toggle="tooltip" data-placement="bottom" title="" data-original-title="The number of Ethereum blocks until the order automatically expires. (14 seconds per block.)">Expires</label>
                        <div class="input-group">
                            <input type="text" class="form-control form-control-sm" id="buyExpires" value="10000">
                            <div class="input-group-append">
                                <span class="input-group-text">Blocks</span>
                            </div>
                        </div>
                    </div>

                    <span class="text-warning"></span>

                    <div class="form-group">
                        <button type="button" class="btn btn-success btn-sm" style="width: 100%;">Buy Order</button>
                    </div>
                </form>
            </div> <!-- tabpanel -->

            <div role="tabpanel" class="tab-pane fade" id="sell">
                <form>
                    <div class="form-group">
                        <label for="sellAmount">Amount to sell</label>
                        <div class="input-group">
                            <input type="text" class="form-control form-control-sm" id="sellAmount">
                            <div class="input-group-append">
                                <span class="input-group-text">BAI</span>
                            </div>
                        </div>
                    </div>

                    <div class="form-group">
                        <label for="sellPrice">Price</label>
                        <div class="input-group">
                            <input type="text" class="form-control form-control-sm" id="sellPrice">
                            <div class="input-group-append">
                                <span class="input-group-text">BCH</span>
                            </div>
                        </div>
                    </div>

                    <div class="form-group">
                        <label for="sellTotal">Total</label>
                        <input type="text" class="form-control form-control-sm" id="sellTotal" value="" readonly="">
                    </div>

                    <div class="form-group">
                        <label for="sellExpires" data-toggle="tooltip" data-placement="bottom" title="" data-original-title="The number of Ethereum blocks until the order automatically expires. (14 seconds per block.)">Expires</label>
                        <div class="input-group">
                            <input type="text" class="form-control form-control-sm" id="sellExpires" value="10000">
                            <div class="input-group-append">
                                <span class="input-group-text">Blocks</span>
                            </div>
                        </div>
                    </div>

                    <span class="text-warning"></span>

                    <div class="form-group">
                        <button type="button" class="btn btn-danger btn-sm" style="width: 100%;">Sell Order</button>
                    </div>
                </form>
            </div> <!-- tabpanel -->
        </div> <!-- tab-content -->
    </div>
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
