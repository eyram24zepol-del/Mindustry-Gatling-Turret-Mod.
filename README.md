# Mindustry-Gatling-Turret-Mod.
A high rate-of-fire turret. Its power and projectile count increase with each ammo tier.
type: Turret
name: automatic-gatling-turret
displayName: Automatic Gatling Turret
description: A high rate-of-fire turret. Its power and projectile count increase with each ammo tier.

// Building requirements
requirements: [
    copper/75
    lead/120
    silicon/80
]
size: 2
health: 400

// Turret properties
rotateSpeed: 10
range: 150
shots: 1
reload: 72
minReload: 4
shootStatus: unmoving
shootStatusDuration: 300
shootType: ShootPatternType
laserColor: [1, 0, 0, 0.75]
laserWidth: 0.5
laserLength: 150

// Ammunition tiers with different projectile counts and effects
ammo: {
    // TIER 1: LEAD AMMO
    lead: {
        bullet: {
            type: BasicBulletType
            damage: 2
            speed: 5
            shots: 1
        }
    }
    
    // TIER 2: COPPER AMMO
    copper: {
        bullet: {
            type: BasicBulletType
            damage: 4
            speed: 6
            lifetime: 25
            shots: 2
        }
    }

    // TIER 3: GRAPHITE AMMO
    graphite: {
        bullet: {
            type: BasicBulletType
            damage: 6
            speed: 7
            lifetime: 22
            splashDamage: 10
            splashDamageRadius: 10
            shots: 3
        }
    }

    // TIER 4: PLASTANIUM AMMO
    plastanium: {
        bullet: {
            type: BasicBulletType
            damage: 8
            speed: 8
            lifetime: 20
            shots: 4
        }
    }

    // TIER 5: GRAND TIER AMMO (SURGE ALLOY)
    surge-alloy: {
        bullet: {
            type: BasicBulletType
            damage: 10
            speed: 9
            lifetime: 20
            pierce: true
            shots: 5
            
            lightning: 3
            lightningLength: 10
            lightningDamage: 15
        }
    }
}
