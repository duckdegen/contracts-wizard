# Snapshot report for `src/custom.test.ts`

The actual snapshot is saved in `custom.test.ts.snap`.

Generated by [AVA](https://avajs.dev).

## custom

> Snapshot 1

    `# SPDX-License-Identifier: MIT␊
    ␊
    %lang starknet␊
    `

## pausable

> Snapshot 1

    `# SPDX-License-Identifier: MIT␊
    ␊
    %lang starknet␊
    ␊
    from starkware.cairo.common.cairo_builtins import HashBuiltin␊
    ␊
    from openzeppelin.security.pausable import Pausable␊
    from openzeppelin.access.ownable import Ownable␊
    ␊
    @constructor␊
    func constructor{␊
            syscall_ptr: felt*,␊
            pedersen_ptr: HashBuiltin*,␊
            range_check_ptr␊
        }(owner: felt):␊
        Ownable.initializer(owner)␊
        return ()␊
    end␊
    ␊
    #␊
    # Getters␊
    #␊
    ␊
    @view␊
    func paused{␊
            syscall_ptr: felt*,␊
            pedersen_ptr: HashBuiltin*,␊
            range_check_ptr␊
        }() -> (paused: felt):␊
        let (paused) = Pausable.is_paused()␊
        return (paused)␊
    end␊
    ␊
    #␊
    # Externals␊
    #␊
    ␊
    @external␊
    func transferOwnership{␊
            syscall_ptr: felt*,␊
            pedersen_ptr: HashBuiltin*,␊
            range_check_ptr␊
        }(newOwner: felt):␊
        Ownable.transfer_ownership(newOwner)␊
        return ()␊
    end␊
    ␊
    @external␊
    func renounceOwnership{␊
            syscall_ptr: felt*,␊
            pedersen_ptr: HashBuiltin*,␊
            range_check_ptr␊
        }():␊
        Ownable.renounce_ownership()␊
        return ()␊
    end␊
    ␊
    @external␊
    func pause{␊
            syscall_ptr: felt*,␊
            pedersen_ptr: HashBuiltin*,␊
            range_check_ptr␊
        }():␊
        Ownable.assert_only_owner()␊
        Pausable._pause()␊
        return ()␊
    end␊
    ␊
    @external␊
    func unpause{␊
            syscall_ptr: felt*,␊
            pedersen_ptr: HashBuiltin*,␊
            range_check_ptr␊
        }():␊
        Ownable.assert_only_owner()␊
        Pausable._unpause()␊
        return ()␊
    end␊
    `

## upgradeable

> Snapshot 1

    `# SPDX-License-Identifier: MIT␊
    ␊
    %lang starknet␊
    ␊
    from starkware.cairo.common.cairo_builtins import HashBuiltin␊
    ␊
    from openzeppelin.upgrades.library import Proxy␊
    ␊
    @external␊
    func initializer{␊
            syscall_ptr: felt*,␊
            pedersen_ptr: HashBuiltin*,␊
            range_check_ptr␊
        }(proxy_admin: felt):␊
        Proxy.initializer(proxy_admin)␊
        return ()␊
    end␊
    ␊
    #␊
    # Externals␊
    #␊
    ␊
    @external␊
    func upgrade{␊
            syscall_ptr: felt*,␊
            pedersen_ptr: HashBuiltin*,␊
            range_check_ptr␊
        }(new_implementation: felt) -> ():␊
        Proxy.assert_only_admin()␊
        Proxy._set_implementation_hash(new_implementation)␊
        return ()␊
    end␊
    `

## access control disabled

> Snapshot 1

    `# SPDX-License-Identifier: MIT␊
    ␊
    %lang starknet␊
    `

## access control ownable

> Snapshot 1

    `# SPDX-License-Identifier: MIT␊
    ␊
    %lang starknet␊
    ␊
    from starkware.cairo.common.cairo_builtins import HashBuiltin␊
    ␊
    from openzeppelin.access.ownable import Ownable␊
    ␊
    @constructor␊
    func constructor{␊
            syscall_ptr: felt*,␊
            pedersen_ptr: HashBuiltin*,␊
            range_check_ptr␊
        }(owner: felt):␊
        Ownable.initializer(owner)␊
        return ()␊
    end␊
    ␊
    #␊
    # Externals␊
    #␊
    ␊
    @external␊
    func transferOwnership{␊
            syscall_ptr: felt*,␊
            pedersen_ptr: HashBuiltin*,␊
            range_check_ptr␊
        }(newOwner: felt):␊
        Ownable.transfer_ownership(newOwner)␊
        return ()␊
    end␊
    ␊
    @external␊
    func renounceOwnership{␊
            syscall_ptr: felt*,␊
            pedersen_ptr: HashBuiltin*,␊
            range_check_ptr␊
        }():␊
        Ownable.renounce_ownership()␊
        return ()␊
    end␊
    `

## pausable with access control disabled

> Snapshot 1

    `# SPDX-License-Identifier: MIT␊
    ␊
    %lang starknet␊
    ␊
    from starkware.cairo.common.cairo_builtins import HashBuiltin␊
    ␊
    from openzeppelin.security.pausable import Pausable␊
    from openzeppelin.access.ownable import Ownable␊
    ␊
    @constructor␊
    func constructor{␊
            syscall_ptr: felt*,␊
            pedersen_ptr: HashBuiltin*,␊
            range_check_ptr␊
        }(owner: felt):␊
        Ownable.initializer(owner)␊
        return ()␊
    end␊
    ␊
    #␊
    # Getters␊
    #␊
    ␊
    @view␊
    func paused{␊
            syscall_ptr: felt*,␊
            pedersen_ptr: HashBuiltin*,␊
            range_check_ptr␊
        }() -> (paused: felt):␊
        let (paused) = Pausable.is_paused()␊
        return (paused)␊
    end␊
    ␊
    #␊
    # Externals␊
    #␊
    ␊
    @external␊
    func transferOwnership{␊
            syscall_ptr: felt*,␊
            pedersen_ptr: HashBuiltin*,␊
            range_check_ptr␊
        }(newOwner: felt):␊
        Ownable.transfer_ownership(newOwner)␊
        return ()␊
    end␊
    ␊
    @external␊
    func renounceOwnership{␊
            syscall_ptr: felt*,␊
            pedersen_ptr: HashBuiltin*,␊
            range_check_ptr␊
        }():␊
        Ownable.renounce_ownership()␊
        return ()␊
    end␊
    ␊
    @external␊
    func pause{␊
            syscall_ptr: felt*,␊
            pedersen_ptr: HashBuiltin*,␊
            range_check_ptr␊
        }():␊
        Ownable.assert_only_owner()␊
        Pausable._pause()␊
        return ()␊
    end␊
    ␊
    @external␊
    func unpause{␊
            syscall_ptr: felt*,␊
            pedersen_ptr: HashBuiltin*,␊
            range_check_ptr␊
        }():␊
        Ownable.assert_only_owner()␊
        Pausable._unpause()␊
        return ()␊
    end␊
    `