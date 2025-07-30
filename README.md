local player = game.Players.LocalPlayer
local mouse = player:GetMouse()

local flying = false
local speed = 50
local bodyGyro
local bodyVelocity

local function startFlying()
	if not flying and player.Character and player.Character:FindFirstChild("HumanoidRootPart") then
		flying = true

		local hrp = player.Character.HumanoidRootPart

		bodyGyro = Instance.new("BodyGyro")
		bodyGyro.P = 9e4
		bodyGyro.maxTorque = Vector3.new(9e9, 9e9, 9e9)
		bodyGyro.cframe = hrp.CFrame
		bodyGyro.Parent = hrp

		bodyVelocity = Instance.new("BodyVelocity")
		bodyVelocity.velocity = Vector3.new(0, 0, 0)
		bodyVeloci
