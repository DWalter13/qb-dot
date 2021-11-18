# qb-dot
Department of Transportation Job For QB-Core using code from qb-trucker and qb-builderjob.

This job is just a base RP job at this state. It will have set work locations with tasks to complete along with a traffic manager.


```lua
Add this job to your qb-core/shared.lua

["dot"] = {
		label = "DOT",
		defaultDuty = true,
		grades = {
            ['0'] = {
                name = "Employee",
                payment = 350
            },
			['1'] = {
                name = "Foreman",
				isboss = true,
                payment = 750
            },
        },
	},



Added to qb-bossmenu/config.lua

['insurance'] = vector3(1913.46, 3685.7, 41.08),



Added to qb-radialmenu/config.lua

["dot"] = {
        {
            id = 'towvehicle',
            title = 'Tow vehicle',
            icon = 'truck-pickup',
            type = 'client',
            event = 'qb-tow:client:TowVehicle',
            shouldClose = true
        }, {
            id = 'toggleduty',
            title = 'Toggle Duty',
            icon = 'info-circle',
            type = 'server',
            event = 'QBCore:ToggleDuty',
            shouldClose = true
        }, {
            id = 'dotobjects',
            title = 'Objects',
            icon = 'road',
            items = {
                {
                    id = 'spawnpion',
                    title = 'Cone',
                    icon = 'exclamation-triangle',
                    type = 'client',
                    event = 'police:client:spawnCone',
                    shouldClose = false
                }, {
                    id = 'spawnhek',
                    title = 'Gate',
                    icon = 'torii-gate',
                    type = 'client',
                    event = 'police:client:spawnBarier',
                    shouldClose = false
                }, {
                    id = 'spawntent',
                    title = 'Tent',
                    icon = 'campground',
                    type = 'client',
                    event = 'police:client:spawnTent',
                    shouldClose = false
                }, {
                    id = 'spawnverlichting',
                    title = 'Lighting',
                    icon = 'lightbulb',
                    type = 'client',
                    event = 'police:client:spawnLight',
                    shouldClose = false
                }, {
                    id = 'deleteobject',
                    title = 'Remove object',
                    icon = 'trash',
                    type = 'client',
                    event = 'police:client:deleteObject',
                    shouldClose = false
                }
            }
        }        
    },