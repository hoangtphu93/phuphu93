# phuphu93

https://github.com/hoangtphu93
Add the button to every tweet. Put this code to the activate:

const { button } = this.adapter.exports;
this.adapter.attachConfig({
  POST: (ctx: any) =>
    button({
      DEFAULT: {
        img: EXAMPLE_IMG,
        tooltip: 'Parse Tweet',
        exec: () => {
          console.log('parsedCtx:', ctx);
        },
      },
    }),
});


#[near_bindgen]
#[derive(BorshDeserialize, BorshSerialize)]
pub struct WhitelistContract {
    /// The account ID of the NEAR Foundation. It allows to whitelist new staking pool accounts.
    /// It also allows to whitelist new Staking Pool Factories, which can whitelist staking pools.
    pub foundation_account_id: AccountId,

    /// The whitelisted account IDs of approved staking pool contracts.
    pub whitelist: LookupSet<AccountId>,

    /// The whitelist of staking pool factories. Any account from this list can whitelist staking
    /// pools.
    pub factory_whitelist: LookupSet<AccountId>,
}
