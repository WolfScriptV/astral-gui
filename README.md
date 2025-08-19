local Rayfield = loadstring(game:HttpGet('https://sirius.menu/rayfield'))()

local Window = Rayfield:CreateWindow({
   Name = "Animal Simulator ASTRAL HUB",
   Icon = 0, -- Icon in Topbar. Can use Lucide Icons (string) or Roblox Image (number). 0 to use no icon (default).
   LoadingTitle = "ASTRAl On Top",
   LoadingSubtitle = "Hub",
   ShowText = "Rayfield", -- for mobile users to unhide rayfield, change if you'd like
   Theme = "Default", -- Check https://docs.sirius.menu/rayfield/configuration/themes

   ToggleUIKeybind = "v", -- The keybind to toggle the UI visibility (string like "K" or Enum.KeyCode)

   DisableRayfieldPrompts = false,
   DisableBuildWarnings = false, -- Prevents Rayfield from warning when the script has a version mismatch with the interface

   ConfigurationSaving = {
      Enabled = true,
      FolderName = nil, -- Create a custom folder for your hub/game
      FileName = "Big Hub"
   },

   Discord = {
      Enabled = false, -- Prompt the user to join your Discord server if their executor supports it
      Invite = "noinvitelink", -- The Discord invite code, do not include discord.gg/. E.g. discord.gg/ ABCD would be ABCD
      RememberJoins = true -- Set this to false to make them join the discord every time they load it up
   },

   KeySystem = false, -- Set this to true to use our key system
   KeySettings = {
      Title = "Untitled",
      Subtitle = "Key System",
      Note = "No method of obtaining the key is provided", -- Use this to tell the user how to get a key
      FileName = "Key", -- It is recommended to use something unique as other scripts using Rayfield may overwrite your key file
      SaveKey = true, -- The user's key will be saved, but if you change the key, they will be unable to use your script
      GrabKeyFromSite = false, -- If this is true, set Key below to the RAW site you would like Rayfield to get the key from
      Key = {"Hello"} -- List of keys that will be accepted by the system, can be RAW file links (pastebin, github etc) or simple strings ("hello","key22")
   }
})

local HomeTab = Window:CreateTab("Home", 4483362458) -- Title, Image

local Button = HomeTab:CreateButton({
   Name = "Anti AFK",
   Callback = function()
wait(0.5)local ba=Instance.new("ScreenGui")
local ca=Instance.new("TextLabel")local da=Instance.new("Frame")
local _b=Instance.new("TextLabel")local ab=Instance.new("TextLabel")ba.Parent=game.CoreGui
ba.ZIndexBehavior=Enum.ZIndexBehavior.Sibling;ca.Parent=ba;ca.Active=true
ca.BackgroundColor3=Color3.new(0.176471,0.176471,0.176471)ca.Draggable=true
ca.Position=UDim2.new(0.698610067,0,0.098096624,0)ca.Size=UDim2.new(0,304,0,52)
ca.Font=Enum.Font.SourceSansSemibold;ca.Text="Anti Afk Kick Script"ca.TextColor3=Color3.new(0,1,1)
ca.TextSize=22;da.Parent=ca
da.BackgroundColor3=Color3.new(0.196078,0.196078,0.196078)da.Position=UDim2.new(0,0,1.0192306,0)
da.Size=UDim2.new(0,304,0,107)_b.Parent=da
_b.BackgroundColor3=Color3.new(0.176471,0.176471,0.176471)_b.Position=UDim2.new(0,0,0.800455689,0)
_b.Size=UDim2.new(0,304,0,21)_b.Font=Enum.Font.Arial;_b.Text="Made By:Ur MOM"
_b.TextColor3=Color3.new(1,1,1)_b.TextSize=20;ab.Parent=da
ab.BackgroundColor3=Color3.new(0.176471,0.176471,0.176471)ab.Position=UDim2.new(0,0,0.158377379,0)
ab.Size=UDim2.new(0,304,0,44)ab.Font=Enum.Font.ArialBold;ab.Text="Status: Script Started"
ab.TextColor3=Color3.new(1,1,1)ab.TextSize=20;local bb=game:service'VirtualUser'
game:service'Players'.LocalPlayer.Idled:connect(function()
bb:CaptureController()bb:ClickButton2(Vector2.new())
ab.Text="You went idle and ROBLOX tried to kick you but we reflected it!"wait(2)ab.Text="Script Re-Enabled"end)
   -- The function that takes place when the button is pressed
   end,
})

local Slider = HomeTab:CreateSlider({
   Name = "Speed",
   Range = {0, 100},
   Increment = 10,
   Suffix = " Speed",
   CurrentValue = 16,
   Flag = "Slider1",
   Callback = function(Value)
      game.Players.LocalPlayer.Character.Humanoid.WalkSpeed = Value
   end,
})

local FarmTab = Window:CreateTab("Farm", 4483362458) -- Title, Image

local FreeTab = Window:CreateTab("Free Tool", 4483362458) -- Title, Image

local Section = FarmTab:CreateSection("-Grind Farm-") -- Section Title

local Toggle = FarmTab:CreateToggle({
   Name = "Farming Grind 5k/Spawn",
   CurrentValue = false,
   Flag = "Toggle1", -- A flag is the identifier for the configuration file, make sure every element has a different flag if you're using configuration saving to ensure no overlaps
   Callback = function(Value)
		isHitting = Value
		if isHitting then
			task.spawn(function()
				while isHitting do
					local player = game:GetService("Players").LocalPlayer
					local level = player:FindFirstChild("leaderstats") and player.leaderstats:FindFirstChild("Level") and player.leaderstats.Level.Value
					
					if level and level < 5000 then
						local dummy = workspace:FindFirstChild("MAP") and workspace.MAP:FindFirstChild("dummies") and workspace.MAP.dummies:FindFirstChild("Dummy")
						if dummy and dummy:FindFirstChild("Humanoid") and dummy:FindFirstChild("HumanoidRootPart") then
							local hrp = player.Character and player.Character:FindFirstChild("HumanoidRootPart")
							if hrp then
								hrp.CFrame = dummy.HumanoidRootPart.CFrame + Vector3.new(0, 0, 5)
							end
							local args = {
								dummy.Humanoid,
								2
							}
							game:GetService("ReplicatedStorage"):WaitForChild("jdskhfsIIIllliiIIIdchgdIiIIIlIlIli"):FireServer(unpack(args))
						end
					else
						local dummy2 = workspace:FindFirstChild("MAP") and workspace.MAP:FindFirstChild("5k_dummies") and workspace.MAP["5k_dummies"]:FindFirstChild("Dummy2")
						if dummy2 and dummy2:FindFirstChild("Humanoid") then
							local hrp = player.Character and player.Character:FindFirstChild("HumanoidRootPart")
							if hrp and dummy2:FindFirstChild("HumanoidRootPart") then
								hrp.CFrame = dummy2.HumanoidRootPart.CFrame + Vector3.new(0, 0, 5)
							end
							local args = {
								dummy2.Humanoid,
								2
							}
							game:GetService("ReplicatedStorage").jdskhfsIIIllliiIIIdchgdIiIIIlIlIli:FireServer(unpack(args))
						end
					end
					task.wait()
				end
			end)
		end
   -- The function that takes place when the toggle is pressed
   -- The variable (Value) is a boolean on whether the toggle is true or false
   end,
})

local Toggle = FarmTab:CreateToggle({
   Name = "NewLightningball Grind 5k/Spawn",
   CurrentValue = false,
   Flag = "Toggle1", -- A flag is the identifier for the configuration file, make sure every element has a different flag if you're using configuration saving to ensure no overlaps
   Callback = function(Value)
    		isHitting = Value
		if isHitting then
			task.spawn(function()
				while isHitting do
					local player = game:GetService("Players").LocalPlayer
					local level = player:FindFirstChild("leaderstats") and player.leaderstats:FindFirstChild("Level") and player.leaderstats.Level.Value

					local dummy = nil
					if level and level < 5000 then
						dummy = workspace:FindFirstChild("MAP") and workspace.MAP:FindFirstChild("dummies") and workspace.MAP.dummies:FindFirstChild("Dummy")
					else
						dummy = workspace:FindFirstChild("MAP") and workspace.MAP:FindFirstChild("5k_dummies") and workspace.MAP["5k_dummies"]:FindFirstChild("Dummy2")
					end

					if dummy and dummy:FindFirstChild("HumanoidRootPart") then
						local args = {
							dummy.HumanoidRootPart.Position,
							"NewLightningball"
						}
						game:GetService("ReplicatedStorage").SkillsInRS.RemoteEvent:FireServer(unpack(args))
					end

					task.wait()
				end
			end)
		end
   -- The function that takes place when the toggle is pressed
   -- The variable (Value) is a boolean on whether the toggle is true or false
   end,
})

local Toggle = FarmTab:CreateToggle({
   Name = "Auto Coin",
   CurrentValue = false,
   Flag = "Toggle1", -- A flag is the identifier for the configuration file, make sure every element has a different flag if you're using configuration saving to ensure no overlaps
   Callback = function(Value)
    isHitting = Value
    
            if isHitting then
                -- Lancer une boucle non bloquante
                task.spawn(function()
                    while isHitting do
game:GetService("ReplicatedStorage"):WaitForChild("Events"):WaitForChild("CoinEvent"):FireServer()
task.wait(0.1) -- Pause
    end
                end)
            end
   -- The function that takes place when the toggle is pressed
   -- The variable (Value) is a boolean on whether the toggle is true or false
   end,
})

local ToggleActive = false  --variable

local ToggleActive = false

-- Liste
local BossList = {
    "CRABBOSS",
    "CENTAUR",
    "BOSSBEAR",
    "BOSSDEER",
    "DragonGiraffe",
    "Griffin",
    "LavaGorilla",
}

local hitvalue= {
    CRABBOSS = 1,  
    CENTAUR = 1, 
    BOSSBEAR = 1, 
    BOSSDEER = 1,
    DragonGiraffe = 1,  
    Griffin = 1,
    LavaGorilla = 1,
}

local Toggle = FarmTab:CreateToggle({
    Name = "Farming No tp Boss",
    CurrentValue = false,
    Flag = "AutoAttackBoss",
    Callback = function(Value)
        ToggleActive = Value
        
        while ToggleActive do
            for _, bossName in ipairs(BossList) do
                local bossNPC = workspace.NPC:FindFirstChild(bossName)
                if bossNPC and bossNPC:FindFirstChild("Humanoid") then
                    local damage = hitvalue[bossName] or 1
                    
                    game:GetService("ReplicatedStorage").jdskhfsIIIllliiIIIdchgdIiIIIlIlIli:FireServer(
                        bossNPC.Humanoid,
                        damage
                    )
                end
            end
            wait()
        end
    end,
})

local PvPTab = Window:CreateTab("PvP", 4483362458) -- Title, Image

local isHitting = false
local players = game:GetService("Players")
local replicatedStorage = game:GetService("ReplicatedStorage")
local player = players.LocalPlayer

-- Fonction pour obtenir le joueur le plus proche
local function getClosestPlayer()
    local closestPlayer = nil
    local shortestDistance = math.huge  -- Une valeur initiale infinie

    -- Parcours de tous les joueurs
    for _, targetPlayer in pairs(players:GetPlayers()) do
        if targetPlayer ~= player and targetPlayer.Character and targetPlayer.Character:FindFirstChild("HumanoidRootPart") then
            local targetPosition = targetPlayer.Character.HumanoidRootPart.Position
            local playerPosition = player.Character.HumanoidRootPart.Position
            local distance = (targetPosition - playerPosition).Magnitude  -- Calcul de la distance

            -- Si cette distance est plus courte que la précédente, on met à jour
            if distance < shortestDistance then
                closestPlayer = targetPlayer
                shortestDistance = distance
            end
        end
    end

    return closestPlayer
end

local function startKillAura()
    isHitting = true
    while isHitting do
        local closestPlayer = getClosestPlayer()  -- Récupère le joueur le plus proche
        if closestPlayer and closestPlayer.Character and closestPlayer.Character:FindFirstChild("Humanoid") then
            local args = {
                [1] = closestPlayer.Character.Humanoid,
                [2] = 1  -- Valeur à envoyer au serveur, peut être ajustée si nécessaire
            }
            -- Appelez la fonction sur le serveur
            replicatedStorage.jdskhfsIIIllliiIIIdchgdIiIIIlIlIli:FireServer(unpack(args))  -- Vérifiez ce nom
        end
        task.wait()  -- Ajoutez une petite attente pour éviter de trop solliciter le serveur
    end
end

local function stopKillAura()
    isHitting = false
end

-- Création du Toggle pour activer/désactiver le kill aura
local Toggle = PvPTab:CreateToggle({
    Name = "kill aura",
    CurrentValue = false,
    Flag = "Toggle1", 
    Callback = function(Value)
        if Value then
            task.spawn(startKillAura)
        else
            stopKillAura()
        end
    end,
})

local Section = FarmTab:CreateSection("Event")

local Button = FarmTab:CreateButton({
   Name = "Get All Cow in shop",
   Callback = function()
    		local ReplicatedStorage = game:GetService("ReplicatedStorage")
local SkinClickEvent = ReplicatedStorage:WaitForChild("Events"):WaitForChild("SkinClickEvent")

for i = 1, 11 do
    local args = {
        "COW" .. i,
        "v2"
    }
    SkinClickEvent:FireServer(unpack(args))
    task.wait(0.1)
end
   -- The function that takes place when the button is pressed
   end,
})

local ScriptTab = Window:CreateTab("Script", 4483362458) -- Title, Image

local Button = ScriptTab:CreateButton({
   Name = "Infinity Yield",
   Callback = function()
loadstring(game:HttpGet(('https://raw.githubusercontent.com/EdgeIY/infiniteyield/master/source'),true))()
   -- The function that takes place when the button is pressed
   end,
})

local Button = ScriptTab:CreateButton({
   Name = "Counter kils",
   Callback = function()
    -- Gui to Lua
-- Version: 3.2

-- Instances:

local ScreenGui = Instance.new("ScreenGui")
local Frame = Instance.new("Frame")
local UICorner = Instance.new("UICorner")
local TextLabel = Instance.new("TextLabel")
local TextLabel_2 = Instance.new("TextLabel")
local TextLabel_3 = Instance.new("TextLabel")
local UICorner_2 = Instance.new("UICorner")
local TextLabel_4 = Instance.new("TextLabel")
local TextButton = Instance.new("TextButton")

--Properties:

ScreenGui.Parent = game.Players.LocalPlayer:WaitForChild("PlayerGui")
ScreenGui.ZIndexBehavior = Enum.ZIndexBehavior.Sibling

Frame.Parent = ScreenGui
Frame.BackgroundColor3 = Color3.fromRGB(47, 47, 47)
Frame.BackgroundTransparency = 0.500
Frame.BorderColor3 = Color3.fromRGB(0, 0, 0)
Frame.BorderSizePixel = 0
Frame.Position = UDim2.new(0.44266054, 0, 0.054502368, 0)
Frame.Size = UDim2.new(0, 216, 0, 103)

UICorner.Parent = Frame

TextLabel.Parent = Frame
TextLabel.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
TextLabel.BackgroundTransparency = 1.000
TextLabel.BorderColor3 = Color3.fromRGB(0, 0, 0)
TextLabel.BorderSizePixel = 0
TextLabel.Position = UDim2.new(0.537037015, 0, 0.349514574, 0)
TextLabel.Size = UDim2.new(0, 71, 0, 50)
TextLabel.Font = Enum.Font.SourceSans
TextLabel.Text = "0"
TextLabel.TextColor3 = Color3.fromRGB(255, 255, 255)
TextLabel.TextSize = 30.000

TextLabel_2.Parent = Frame
TextLabel_2.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
TextLabel_2.BackgroundTransparency = 1.000
TextLabel_2.BorderColor3 = Color3.fromRGB(0, 0, 0)
TextLabel_2.BorderSizePixel = 0
TextLabel_2.Position = UDim2.new(0.157407403, 0, 0.349514574, 0)
TextLabel_2.Size = UDim2.new(0, 82, 0, 50)
TextLabel_2.Font = Enum.Font.SourceSans
TextLabel_2.Text = "KILLS:"
TextLabel_2.TextColor3 = Color3.fromRGB(255, 255, 255)
TextLabel_2.TextSize = 30.000

TextLabel_3.Parent = Frame
TextLabel_3.BackgroundColor3 = Color3.fromRGB(76, 76, 76)
TextLabel_3.BackgroundTransparency = 0.200
TextLabel_3.BorderColor3 = Color3.fromRGB(0, 0, 0)
TextLabel_3.BorderSizePixel = 0
TextLabel_3.Size = UDim2.new(0, 216, 0, 36)
TextLabel_3.Font = Enum.Font.SourceSansBold
TextLabel_3.Text = "Kill counter"
TextLabel_3.TextColor3 = Color3.fromRGB(255, 255, 255)
TextLabel_3.TextSize = 35.000

local function updateKillCount()
    local player = game.Players.LocalPlayer
    if player and player:FindFirstChild("otherstats") and player.otherstats:FindFirstChild("Kill") then
        TextLabel.Text = tostring(player.otherstats.Kill.Value)
    else
        TextLabel.Text = "0"
    end
end

updateKillCount()

local killStat
local player = game.Players.LocalPlayer

if player then
    player:WaitForChild("otherstats"):WaitForChild("Kill")
    killStat = player.otherstats.Kill
    killStat:GetPropertyChangedSignal("Value"):Connect(updateKillCount)
end

UICorner_2.Parent = TextLabel_3

TextLabel_4.Parent = Frame
TextLabel_4.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
TextLabel_4.BackgroundTransparency = 1.000
TextLabel_4.BorderColor3 = Color3.fromRGB(0, 0, 0)
TextLabel_4.BorderSizePixel = 0
TextLabel_4.Position = UDim2.new(0.666666687, 0, 0.669902921, 0)
TextLabel_4.Size = UDim2.new(0, 72, 0, 34)
TextLabel_4.Font = Enum.Font.SourceSans
TextLabel_4.Text = "By s0ul"
TextLabel_4.TextColor3 = Color3.fromRGB(255, 255, 255)
TextLabel_4.TextSize = 17.000

TextButton.Parent = Frame
TextButton.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
TextButton.BackgroundTransparency = 1.000
TextButton.BorderColor3 = Color3.fromRGB(0, 0, 0)
TextButton.BorderSizePixel = 0
TextButton.Position = UDim2.new(0.833375692, 0, -0.00730451569, 0)
TextButton.Size = UDim2.new(0, 49, 0, 39)
TextButton.Font = Enum.Font.SourceSans
TextButton.Text = "X"
TextButton.TextColor3 = Color3.fromRGB(213, 0, 0)
TextButton.TextSize = 20.000

-- Scripts:

local function FFPC_fake_script() -- TextButton.LocalScript 
	local script = Instance.new('LocalScript', TextButton)

	local Frame = script.Parent.Parent
	
	script.Parent.MouseButton1Click:Connect(function()
		Frame.Visible = false
	end)
end
coroutine.wrap(FFPC_fake_script)()

   -- The function that takes place when the button is pressed
   end,
})

-- Services
local Players = game:GetService("Players")
local player = Players.LocalPlayer
local FightingZone = workspace.FightingArea.FightingZonePart2 -- <-- mise à jour ici

-- Helpers
local function isAlive(p)
    local ch = p.Character
    local hum = ch and ch:FindFirstChildOfClass("Humanoid")
    return hum and hum.Health > 0
end

local function hasHRP(p)
    local ch = p.Character
    return ch and ch:FindFirstChild("HumanoidRootPart") ~= nil
end

local function isInZone(p)
    local ch = p.Character
    local hrp = ch and ch:FindFirstChild("HumanoidRootPart")
    if not hrp then return false end
    local min = FightingZone.Position - FightingZone.Size/2
    local max = FightingZone.Position + FightingZone.Size/2
    local pos = hrp.Position
    return (pos.X > min.X and pos.X < max.X)
        and (pos.Y > min.Y and pos.Y < max.Y)
        and (pos.Z > min.Z and pos.Z < max.Z)
end

local function validTargets()
    local list = {}
    for _, t in ipairs(Players:GetPlayers()) do
        if t ~= player and isAlive(t) and hasHRP(t) and (not isInZone(t)) then
            table.insert(list, t)
        end
    end
    return list
end

local function nextTarget(current)
    local list = validTargets()
    if #list == 0 then return nil end
    if not current then return list[1] end
    local idx
    for i, pl in ipairs(list) do
        if pl == current then idx = i break end
    end
    if not idx then return list[1] end
    if #list == 1 then return nil end
    local nextIdx = (idx % #list) + 1
    return list[nextIdx]
end

local function teleportTo(targetPlayer)
    local myChar = player.Character or player.CharacterAdded:Wait()
    local myHRP = myChar:WaitForChild("HumanoidRootPart")
    local tChar = targetPlayer.Character
    local tHRP = tChar and tChar:FindFirstChild("HumanoidRootPart")
    if tHRP then
        myHRP.CFrame = tHRP.CFrame + Vector3.new(0, 5, 0)
        return true
    end
    return false
end

-- Variables
local tpEnabled = false
local currentTarget = nil
local tpDelay = 1

-- Toggle Auto TP
local Toggle = HomeTab:CreateToggle({
   Name = "Auto TP Players",
   CurrentValue = false,
   Flag = "Toggle1",
   Callback = function(Value)
      tpEnabled = Value
      if tpEnabled then
         task.spawn(function()
            while tpEnabled do
                if (not currentTarget)
                    or (not isAlive(currentTarget))
                    or (not hasHRP(currentTarget))
                    or isInZone(currentTarget) then
                    currentTarget = nextTarget(currentTarget)
                end

                if currentTarget and not isInZone(currentTarget) then
                    teleportTo(currentTarget)
                end

                task.wait(tpDelay)
            end
         end)
      else
         currentTarget = nil
      end
   end,
})

-- Bouton Skip
local Button = HomeTab:CreateButton({
   Name = "Skip Player",
   Callback = function()
      if not tpEnabled then return end
      local nxt = nextTarget(currentTarget)
      if nxt then
         currentTarget = nxt
         teleportTo(currentTarget)
      end
   end,
})


local ToggleActive = false

local BossList = {
    "CRABBOSS",
    "CENTAUR",
    "BOSSBEAR",
    "BOSSDEER",
    "DragonGiraffe",
    "Griffin",
    "LavaGorilla",
}

local hitvalue= {
    CRABBOSS = 1,  
    CENTAUR = 1, 
    BOSSBEAR = 1, 
    BOSSDEER = 1,
    DragonGiraffe = 1,  
    Griffin = 1,
    LavaGorilla = 1,
}

local Toggle = HomeTab:CreateToggle({
    Name = "Farming tp Boss",
    CurrentValue = false,
    Flag = "AutoAttackBoss",
    Callback = function(Value)
        ToggleActive = Value

        task.spawn(function()
            local player = game.Players.LocalPlayer
            local bossIndex = 1

            while ToggleActive do
                if #BossList == 0 then break end
                local bossName = BossList[bossIndex]
                local bossNPC = workspace.NPC:FindFirstChild(bossName)

                if bossNPC and bossNPC:FindFirstChild("Humanoid") and bossNPC:FindFirstChild("HumanoidRootPart") then
                    local hum = bossNPC.Humanoid
                    local hrp = bossNPC.HumanoidRootPart

                    -- Crée la Part si elle n'existe pas
                    local partName = bossName .. "_Part"
                    local part = workspace:FindFirstChild(partName)
                    if not part then
                        part = Instance.new("Part")
                        part.Name = partName
                        part.Size = Vector3.new(10,1,10)
                        part.Anchored = true
                        part.CanCollide = true
                        part.Position = hrp.Position + Vector3.new(0,10,0)
                        part.Color = Color3.fromRGB(255,0,0)
                        part.Parent = workspace
                    end

                    -- Met la vie du boss à 1
                    if hum.Health > 1 then
                        hum.Health = 1
                    end

                    -- TP le joueur sur la Part et bloque-le
                    if player.Character and player.Character:FindFirstChild("HumanoidRootPart") then
                        player.Character.HumanoidRootPart.CFrame = part.CFrame + Vector3.new(0,3,0)
                        player.Character.Humanoid.PlatformStand = true
                    end

                    -- Envoie un petit dégât pour que le kill soit compté
                    local damage = hitvalue[bossName] or 1
                    local remote = game:GetService("ReplicatedStorage"):FindFirstChild("jdskhfsIIIllliiIIIdchgdIiIIIlIlIli")
                    if remote then
                        remote:FireServer(hum, damage)
                    end

                    -- Met à jour la position de la Part pour suivre le boss
                    part.Position = hrp.Position + Vector3.new(0,10,0)

                    -- Tant que le boss n'est pas mort, on reste dessus
                    while hum.Health > 0 and ToggleActive do
                        if player.Character and player.Character:FindFirstChild("HumanoidRootPart") then
                            player.Character.HumanoidRootPart.CFrame = part.CFrame + Vector3.new(0,3,0)
                        end
                        -- Part suit le boss
                        part.Position = hrp.Position + Vector3.new(0,10,0)
                        task.wait(0.1)
                    end
                end

                -- Passe au boss suivant si toggle toujours actif
                bossIndex = bossIndex + 1
                if bossIndex > #BossList then
                    bossIndex = 1 -- revient au premier boss si tous tués
                end
                task.wait(0.2)
            end

            -- Redonne le contrôle quand toggle désactivé
            if player.Character and player.Character:FindFirstChild("Humanoid") then
                player.Character.Humanoid.PlatformStand = false
            end
        end)
    end,
})


local Players = game:GetService("Players")
local RunService = game:GetService("RunService")
local LocalPlayer = Players.LocalPlayer
local Character = LocalPlayer.Character or LocalPlayer.CharacterAdded:Wait()
local HumanoidRootPart = Character:WaitForChild("HumanoidRootPart")
local Humanoid = Character:WaitForChild("Humanoid")

-- Variable pour stocker le joueur sélectionné
local targetPlayerName = nil
local followPart = nil

-- Fonction pour récupérer tous les joueurs sauf toi
local function getPlayerNames()
    local names = {}
    for _, player in pairs(Players:GetPlayers()) do
        if player ~= LocalPlayer then
            table.insert(names, player.Name)
        end
    end
    return names
end

-- Dropdown pour choisir un joueur
local Dropdown = HomeTab:CreateDropdown({
    Name = "Players Dropdown",
    Options = getPlayerNames(),
    CurrentOption = {},
    MultipleOptions = false,
    Flag = "Dropdown1",
    Callback = function(Options)
        targetPlayerName = Options[1]
    end,
})

-- Mettre à jour le Dropdown automatiquement
Players.PlayerAdded:Connect(function()
    Dropdown:Update(getPlayerNames())
end)
Players.PlayerRemoving:Connect(function(player)
    Dropdown:Update(getPlayerNames())
    if targetPlayerName == player.Name then
        targetPlayerName = nil
    end
end)

-- Toggle pour créer le Part au-dessus du joueur et te bloquer dessus
local Toggle = HomeTab:CreateToggle({
    Name = "Block On Player",
    CurrentValue = false,
    Flag = "Toggle1",
    Callback = function(Value)
        if Value then
            if targetPlayerName then
                local target = Players:FindFirstChild(targetPlayerName)
                if target and target.Character and target.Character:FindFirstChild("HumanoidRootPart") then
                    local targetHRP = target.Character.HumanoidRootPart

                    -- Crée le Part au-dessus du joueur
                    followPart = Instance.new("Part")
                    followPart.Size = Vector3.new(4,1,4)
                    followPart.Anchored = true
                    followPart.CanCollide = true
                    followPart.Position = targetHRP.Position + Vector3.new(0, 5, 0) -- 5 studs au-dessus
                    followPart.Parent = workspace

                    -- Bloque le joueur sur le Part
                    HumanoidRootPart.CFrame = followPart.CFrame
                    Humanoid.PlatformStand = true -- empêche de bouger

                    -- Met à jour la position du Part à chaque frame
                    local connection
                    connection = RunService.RenderStepped:Connect(function()
                        if not Toggle.CurrentValue then
                            connection:Disconnect()
                            followPart:Destroy()
                            Humanoid.PlatformStand = false
                            return
                        end
                        followPart.Position = targetHRP.Position + Vector3.new(0, 5, 0)
                        HumanoidRootPart.CFrame = followPart.CFrame
                    end)
                end
            end
        else
            -- Désactivation
            if followPart then
                followPart:Destroy()
                followPart = nil
                Humanoid.PlatformStand = false
            end
        end
    end,
})
