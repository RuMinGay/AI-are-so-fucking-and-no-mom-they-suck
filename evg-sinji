writefile("cruelangel.mp3", game:HttpGet("https://github.com/RuMinGay/Ai-are-so-fucking-and-no-mom-they-suck/raw/refs/heads/main/cruelangel.mp3"))     
local sound = nil
        sound = Instance.new("Sound")
        sound.SoundId = getcustomasset("cruelangel.mp3")
        sound.Volume = 3
        sound.Looped = true
        sound.Parent = game.workspace
        sound:Play()
        local Players = game:GetService("Players")
local LocalPlayer = Players.LocalPlayer

local ANIMATION_SOUND_MAP = {
    ["rbxassetid://13370310513"] = "rbxassetid://18511965048",
    ["rbxassetid://13390230973"] = "rbxassetid://7118966167", 
    ["rbxassetid://13378708199"] = "rbxassetid://13294122648" 
}

local function setupCharacter(character)
    local humanoid = character:WaitForChild("Humanoid", 10)
    local animator = humanoid and humanoid:WaitForChild("Animator", 10)
    if not animator then
        return
    end

    local connection
    connection = animator.AnimationPlayed:Connect(function(animationTrack)
        local animationId = animationTrack.Animation.AnimationId
        local soundId = ANIMATION_SOUND_MAP[animationId]
        if soundId then
            local sound = Instance.new("Sound")
            sound.SoundId = soundId
            sound.Parent = character
            sound.Volume = 2
            sound:Play()
            
            sound.Ended:Connect(function()
                sound:Destroy()
            end)
        end
    end)

    character.AncestryChanged:Connect(function()
        if not character:IsDescendantOf(game) then
            connection:Disconnect()
        end
    end)
end

if LocalPlayer.Character then
    task.spawn(function()
        setupCharacter(LocalPlayer.Character)
    end)
end

LocalPlayer.CharacterAdded:Connect(function(character)
    task.spawn(function()
        setupCharacter(character)
    end)
end)
task.wait(2)
        local Players = game:GetService("Players")
local LocalPlayer = Players.LocalPlayer
local Character = LocalPlayer.Character or LocalPlayer.CharacterAdded:Wait()
local HumanoidRootPart = Character:WaitForChild("HumanoidRootPart")
local Debris = game:GetService("Debris")

local function createShinjiEffect()
    local effectPart = Instance.new("Part")
    effectPart.Size = Vector3.new(5, 5, 5)
    effectPart.Transparency = 1
    effectPart.CanCollide = false
    effectPart.Anchored = false
    effectPart.CFrame = HumanoidRootPart.CFrame
    effectPart.Parent = workspace

    local particleEmitter = Instance.new("ParticleEmitter")
    particleEmitter.Color = ColorSequence.new(Color3.fromRGB(255, 0, 0), Color3.fromRGB(255, 100, 100))
    particleEmitter.Rate = 500
    particleEmitter.Lifetime = NumberRange.new(0.5, 1.5)
    particleEmitter.Speed = NumberRange.new(5, 10)
    particleEmitter.SpreadAngle = Vector2.new(360, 360)
    particleEmitter.Transparency = NumberSequence.new(0, 0.5, 1)
    particleEmitter.Size = NumberSequence.new(0.5, 1)
    particleEmitter.Parent = effectPart

    local camera = workspace.CurrentCamera
    local originalCFrame = camera.CFrame
    local shakeIntensity = 0.2
    local shakeDuration = 1.0

    for i = 1, math.floor(shakeDuration * 60) do
        local offsetX = math.random() * shakeIntensity * 2 - shakeIntensity
        local offsetY = math.random() * shakeIntensity * 2 - shakeIntensity
        local offsetZ = math.random() * shakeIntensity * 2 - shakeIntensity
        camera.CFrame = originalCFrame * CFrame.new(offsetX, offsetY, offsetZ)
        task.wait()
    end
    camera.CFrame = originalCFrame

    Debris:AddItem(effectPart, 6)
end

createShinjiEffect()

LocalPlayer.CharacterAdded:Connect(function(newCharacter)
    Character = newCharacter
    HumanoidRootPart = Character:WaitForChild("HumanoidRootPart")
end)
local Players = game:GetService("Players")
local TweenService = game:GetService("TweenService")
local LocalPlayer = Players.LocalPlayer

function enabledpart1()
local Players = game:GetService("Players")
local RunService = game:GetService("RunService")
local LocalPlayer = Players.LocalPlayer
    local character = LocalPlayer.Character
    if not character or not character.Parent then
        return
    end

    local targetLimb = character:FindFirstChild("RightHand")
    if not targetLimb then
        targetLimb = character:FindFirstChild("Right Arm")
    end

    if not targetLimb then
        targetLimb = character:WaitForChild("RightHand", 0.5) or character:WaitForChild("Right Arm", 0.5)
    end

    if not targetLimb then
        return
    end

    local existingSword = character:FindFirstChild("PlayerSwordModel")
    if existingSword then existingSword:Destroy() end

    local swordModel = Instance.new("Model")
    swordModel.Name = "PlayerSwordModel"
    swordModel.Parent = character

    local blade = Instance.new("Part")
    blade.Name = "Blade"
    blade.Size = Vector3.new(0.3, 3, 0.1)
    blade.Color = Color3.fromRGB(180, 180, 180)
    blade.Material = Enum.Material.Metal
    blade.CanCollide = false
    blade.Anchored = false
    blade.Massless = true
    blade.Parent = swordModel

    local guard = Instance.new("Part")
    guard.Name = "Guard"
    guard.Size = Vector3.new(0.5, 0.2, 0.8)
    guard.Color = Color3.fromRGB(120, 120, 120)
    guard.Material = Enum.Material.Metal
    guard.CanCollide = false
    guard.Anchored = false
    guard.Massless = true
    guard.Parent = swordModel
    guard.Position = Vector3.new(0, -1.5, 0)

    local handle = Instance.new("Part")
    handle.Name = "Handle"
    handle.Size = Vector3.new(0.2, 1.5, 0.2)
    handle.Color = Color3.fromRGB(50, 50, 50)
    handle.Material = Enum.Material.SmoothPlastic
    handle.CanCollide = false
    handle.Anchored = false
    handle.Massless = true
    handle.Parent = swordModel
    handle.Position = Vector3.new(0, -2.25, 0)

    local bladeWeldGuard = Instance.new("Weld")
    bladeWeldGuard.Part0 = blade
    bladeWeldGuard.Part1 = guard
    bladeWeldGuard.C0 = CFrame.new(0, -1.5, 0)
    bladeWeldGuard.Parent = blade

    local bladeWeldHandle = Instance.new("Weld")
    bladeWeldHandle.Part0 = blade
    bladeWeldHandle.Part1 = handle
    bladeWeldHandle.C0 = CFrame.new(0, -2.25, 0)
    bladeWeldHandle.Parent = blade

    swordModel.PrimaryPart = blade

    local mainWeld = Instance.new("Weld")
    mainWeld.Name = "MainSwordWeld"
    mainWeld.Part0 = targetLimb
    mainWeld.Part1 = swordModel.PrimaryPart

    if targetLimb.Name == "RightHand" then
        mainWeld.C1 = CFrame.new(0.3, 0.0, 11) * CFrame.Angles(math.rad(-90), math.rad(-180), math.rad(180))
    else
        mainWeld.C1 = CFrame.new(0, -2.7, 1) * CFrame.Angles(math.rad(-90), math.rad(-180), math.rad(180))
    end
    mainWeld.Parent = swordModel.PrimaryPart
end

local Players = game:GetService("Players")
local TweenService = game:GetService("TweenService")
local LocalPlayer = Players.LocalPlayer

function enabledpart()

    local targetLimb = character:FindFirstChild("RightHand")
    if not targetLimb then
        targetLimb = character:FindFirstChild("Right Arm")
    end

    if not targetLimb then
        targetLimb = character:WaitForChild("RightHand", 0.5) or character:WaitForChild("Right Arm", 0.5)
    end

    if not targetLimb then
        return
    end

    local existingSword = character:FindFirstChild("PlayerSwordModel")
    if existingSword then existingSword:Destroy() end

    local swordModel = Instance.new("Model")
    swordModel.Name = "PlayerSwordModel"
    swordModel.Parent = character

    local blade = Instance.new("Part")
    blade.Name = "Blade"
    blade.Size = Vector3.new(0.3, 3, 0.1)
    blade.Color = Color3.fromRGB(180, 180, 180)
    blade.Material = Enum.Material.Metal
    blade.CanCollide = false
    blade.Anchored = false
    blade.Massless = true
    blade.Parent = swordModel

    local guard = Instance.new("Part")
    guard.Name = "Guard"
    guard.Size = Vector3.new(0.5, 0.2, 0.8)
    guard.Color = Color3.fromRGB(120, 120, 120)
    guard.Material = Enum.Material.Metal
    guard.CanCollide = false
    guard.Anchored = false
    guard.Massless = true
    guard.Parent = swordModel
    guard.Position = Vector3.new(0, -1.5, 0)

    local handle = Instance.new("Part")
    handle.Name = "Handle"
    handle.Size = Vector3.new(0.2, 1.5, 0.2)
    handle.Color = Color3.fromRGB(50, 50, 50)
    handle.Material = Enum.Material.SmoothPlastic
    handle.CanCollide = false
    handle.Anchored = false
    handle.Massless = true
    handle.Parent = swordModel
    handle.Position = Vector3.new(0, -2.25, 0)

    local bladeWeldGuard = Instance.new("Weld")
    bladeWeldGuard.Part0 = blade
    bladeWeldGuard.Part1 = guard
    bladeWeldGuard.C0 = CFrame.new(0, -1.5, 0)
    bladeWeldGuard.Parent = blade

    local bladeWeldHandle = Instance.new("Weld")
    bladeWeldHandle.Part0 = blade
    bladeWeldHandle.Part1 = handle
    bladeWeldHandle.C0 = CFrame.new(0, -2.25, 0)
    bladeWeldHandle.Parent = blade

    swordModel.PrimaryPart = blade

    local mainWeld = Instance.new("Weld")
    mainWeld.Name = "MainSwordWeld"
    mainWeld.Part0 = targetLimb
    mainWeld.Part1 = swordModel.PrimaryPart

    if targetLimb.Name == "RightHand" then
        mainWeld.C1 = CFrame.new(0.3, 0.0, 11) * CFrame.Angles(math.rad(-90), math.rad(-180), math.rad(180))
    else
        mainWeld.C1 = CFrame.new(0, -2.7, 1) * CFrame.Angles(math.rad(-90), math.rad(-180), math.rad(180))
    end
    mainWeld.Parent = swordModel.PrimaryPart
end

function disabledpart1()
    local character = LocalPlayer.Character or LocalPlayer.CharacterAdded:Wait()
    local humanoid = character:WaitForChild("Humanoid")

    local AnimAnim = Instance.new("Animation")
    AnimAnim.AnimationId = "rbxassetid://13377153603"

    local animator = humanoid:FindFirstChildOfClass("Animator") or Instance.new("Animator")
    animator.Parent = humanoid

    local Anim = animator:LoadAnimation(AnimAnim)
    Anim.Looped = false
    Anim.Priority = Enum.AnimationPriority.Action

    Anim:Play()
    Anim:AdjustSpeed(0.899)
    Anim.TimePosition = 0.05

    local soundId = "rbxassetid://481731911"
    local head = character:WaitForChild("Head") 
    local boomSound = Instance.new("Sound")
    boomSound.SoundId = soundId
    boomSound.Parent = head
    boomSound.Volume = 1
    boomSound:Play()

    boomSound.Ended:Connect(function()
        boomSound:Destroy()
    end)
    task.wait(0.56)

    local swordModel = character:FindFirstChild("PlayerSwordModel")
    if not swordModel then return end

    local torso = character:FindFirstChild("Torso")
    if not torso then
        swordModel:Destroy()
        return
    end

    local mainWeld = swordModel.PrimaryPart:FindFirstChild("MainSwordWeld")
    if not mainWeld then
        swordModel:Destroy()
        return
    end

    mainWeld:Destroy()

    local backWeld = Instance.new("Weld")
    backWeld.Name = "BackSwordWeld"
    backWeld.Part0 = torso
    backWeld.Part1 = swordModel.PrimaryPart

    backWeld.C1 = CFrame.new(-0.5, -0, 0) * 
                  CFrame.Angles(
                      math.rad(0), 
                      math.rad(90),
                      math.rad(-135)  
                  )
    backWeld.Parent = swordModel.PrimaryPart
end
enabledpart1()
task.wait()
disabledpart1()
local Players = game:GetService("Players")
local LocalPlayer = Players.LocalPlayer
local TweenService = game:GetService("TweenService")

local FADE_IN_DURATION = 2

local BLACK_SCREEN_HOLD_DURATION = 3

local FADE_OUT_DURATION = 2

if not LocalPlayer then
    return
end

local PlayerGui = LocalPlayer:WaitForChild("PlayerGui")

local function createFadingBlackScreen()

    for _, gui in ipairs(PlayerGui:GetChildren()) do
        if gui:IsA("ScreenGui") and gui.Name == "FadingBlackScreen" then
            gui:Destroy()
        end
    end

    local blackScreen = Instance.new("ScreenGui")
    blackScreen.Name = "FadingBlackScreen"
    blackScreen.Parent = PlayerGui

    local blackFrame = Instance.new("Frame")
    blackFrame.Name = "BlackFrame"
    blackFrame.Size = UDim2.new(1, 0, 1, 0)
    blackFrame.BackgroundColor3 = Color3.new(0, 0, 0)
    blackFrame.BackgroundTransparency = 1
    blackFrame.ZIndex = 100
    blackFrame.Parent = blackScreen

    local fadeInTweenInfo = TweenInfo.new(FADE_IN_DURATION, Enum.EasingStyle.Quad, Enum.EasingDirection.Out)
    local fadeInGoal = {BackgroundTransparency = 0}
    local fadeInTween = TweenService:Create(blackFrame, fadeInTweenInfo, fadeInGoal)

    fadeInTween:Play()

    fadeInTween.Completed:Wait()

    task.wait(BLACK_SCREEN_HOLD_DURATION)

    local fadeOutTweenInfo = TweenInfo.new(FADE_OUT_DURATION, Enum.EasingStyle.Quad, Enum.EasingDirection.In)
    local fadeOutGoal = {BackgroundTransparency = 1}
    local fadeOutTween = TweenService:Create(blackFrame, fadeOutTweenInfo, fadeOutGoal)
local Players = game:GetService("Players")
local player = Players.LocalPlayer -- 로컬 플레이어 가져오기
local character = player.Character or player.CharacterAdded:Wait() -- 플레이어의 캐릭터 가져오기
local humanoidRootPart = character:WaitForChild("HumanoidRootPart") -- HumanoidRootPart 기다리기

local originalCFrame
if humanoidRootPart then
    originalCFrame = humanoidRootPart.CFrame
    task.wait()
    local targetCFrame = CFrame.new(438.040100, 439.511932, -376.26217)

for i=1, 3 do
local player = game.Players.LocalPlayer
local playerGui = player:WaitForChild("PlayerGui")
local screenGui = Instance.new("ScreenGui")
screenGui.Name = "Dasa"
screenGui.Parent = playerGui
local textLabel = Instance.new("TextLabel")
textLabel.Name = "Dasa1"
textLabel.Size = UDim2.new(0.3, 0, 0.1, 0)
textLabel.Position = UDim2.new(0.5, 0, 0.5, 0)
textLabel.AnchorPoint = Vector2.new(0.5, 0.5)
textLabel.BackgroundTransparency = 1
textLabel.Text = "I mustn't run away... I mustn't run away... I mustn't run away!"
textLabel.TextColor3 = Color3.fromRGB(250, 0, 0)
textLabel.TextScaled = true
textLabel.Font = Enum.Font.SourceSansBold
textLabel.ZIndex = 2521321312321312321
textLabel.Parent = screenGui
task.wait(0.1)
screenGui:Destroy()
local player = game.Players.LocalPlayer
local playerGui = player:WaitForChild("PlayerGui")
local screenGui = Instance.new("ScreenGui")
screenGui.Name = "Dasa"
screenGui.Parent = playerGui
local textLabel = Instance.new("TextLabel")
textLabel.Name = "Dasa1"
textLabel.Size = UDim2.new(0.3, 0, 0.1, 0)
textLabel.Position = UDim2.new(0.5, 0, 0.5, 0)
textLabel.AnchorPoint = Vector2.new(0.5, 0.5)
textLabel.BackgroundTransparency = 1
textLabel.Text = "Is this... my solitude?"
textLabel.TextColor3 = Color3.fromRGB(250, 0, 0)
textLabel.TextScaled = true
textLabel.Font = Enum.Font.SourceSansBold
textLabel.ZIndex = 2521321312321312321
textLabel.Parent = screenGui
task.wait(0.1)
screenGui:Destroy()
local player = game.Players.LocalPlayer
local playerGui = player:WaitForChild("PlayerGui")
local screenGui = Instance.new("ScreenGui")
screenGui.Name = "Dasa"
screenGui.Parent = playerGui
local textLabel = Instance.new("TextLabel")
textLabel.Name = "Dasa1"
textLabel.Size = UDim2.new(0.3, 0, 0.1, 0)
textLabel.Position = UDim2.new(0.5, 0, 0.5, 0)
textLabel.AnchorPoint = Vector2.new(0.5, 0.5)
textLabel.BackgroundTransparency = 1
textLabel.Text = "If you do nothing, nothing will happen."
textLabel.TextColor3 = Color3.fromRGB(250, 0, 0)
textLabel.TextScaled = true
textLabel.Font = Enum.Font.SourceSansBold
textLabel.ZIndex = 2521321312321312321
textLabel.Parent = screenGui
task.wait(0.1)
screenGui:Destroy()
local player = game.Players.LocalPlayer
local playerGui = player:WaitForChild("PlayerGui")
local screenGui = Instance.new("ScreenGui")
screenGui.Name = "Dasa"
screenGui.Parent = playerGui
local textLabel = Instance.new("TextLabel")
textLabel.Name = "Dasa1"
textLabel.Size = UDim2.new(0.3, 0, 0.1, 0)
textLabel.Position = UDim2.new(0.5, 0, 0.5, 0)
textLabel.AnchorPoint = Vector2.new(0.5, 0.5)
textLabel.BackgroundTransparency = 1
textLabel.Text = "I am me. I am not me."
textLabel.TextColor3 = Color3.fromRGB(250, 0, 0)
textLabel.TextScaled = true
textLabel.Font = Enum.Font.SourceSansBold
textLabel.ZIndex = 2521321312321312321
textLabel.Parent = screenGui
task.wait(0.1)
screenGui:Destroy()
local player = game.Players.LocalPlayer
local playerGui = player:WaitForChild("PlayerGui")
local screenGui = Instance.new("ScreenGui")
screenGui.Name = "Dasa"
screenGui.Parent = playerGui
local textLabel = Instance.new("TextLabel")
textLabel.Name = "Dasa1"
textLabel.Size = UDim2.new(0.3, 0, 0.1, 0)
textLabel.Position = UDim2.new(0.5, 0, 0.5, 0)
textLabel.AnchorPoint = Vector2.new(0.5, 0.5)
textLabel.BackgroundTransparency = 1
textLabel.Text = "Sometimes, I just don't know where to put my hands"
textLabel.TextColor3 = Color3.fromRGB(250, 0, 0)
textLabel.TextScaled = true
textLabel.Font = Enum.Font.SourceSansBold
textLabel.ZIndex = 2521321312321312321
textLabel.Parent = screenGui
task.wait(0.1)
screenGui:Destroy()
local player = game.Players.LocalPlayer
local playerGui = player:WaitForChild("PlayerGui")
local screenGui = Instance.new("ScreenGui")
screenGui.Name = "Dasa"
screenGui.Parent = playerGui
local textLabel = Instance.new("TextLabel")
textLabel.Name = "Dasa1"
textLabel.Size = UDim2.new(0.3, 0, 0.1, 0)
textLabel.Position = UDim2.new(0.5, 0, 0.5, 0)
textLabel.AnchorPoint = Vector2.new(0.5, 0.5)
textLabel.BackgroundTransparency = 1
textLabel.Text = "I understand. But I don't understand."
textLabel.TextColor3 = Color3.fromRGB(250, 0, 0)
textLabel.TextScaled = true
textLabel.Font = Enum.Font.SourceSansBold
textLabel.ZIndex = 2521321312321312321
textLabel.Parent = screenGui
task.wait(0.1)
screenGui:Destroy()
local player = game.Players.LocalPlayer
local playerGui = player:WaitForChild("PlayerGui")
local screenGui = Instance.new("ScreenGui")
screenGui.Name = "Dasa"
screenGui.Parent = playerGui
local textLabel = Instance.new("TextLabel")
textLabel.Name = "Dasa1"
textLabel.Size = UDim2.new(0.3, 0, 0.1, 0)
textLabel.Position = UDim2.new(0.5, 0, 0.5, 0)
textLabel.AnchorPoint = Vector2.new(0.5, 0.5)
textLabel.BackgroundTransparency = 1
textLabel.Text = "I just... want to survive."
textLabel.TextColor3 = Color3.fromRGB(250, 0, 0)
textLabel.TextScaled = true
textLabel.Font = Enum.Font.SourceSansBold
textLabel.ZIndex = 2521321312321312321
textLabel.Parent = screenGui
task.wait(0.1)
screenGui:Destroy()
local player = game.Players.LocalPlayer
local playerGui = player:WaitForChild("PlayerGui")
local screenGui = Instance.new("ScreenGui")
screenGui.Name = "Dasa"
screenGui.Parent = playerGui
local textLabel = Instance.new("TextLabel")
textLabel.Name = "Dasa1"
textLabel.Size = UDim2.new(0.3, 0, 0.1, 0)
textLabel.Position = UDim2.new(0.5, 0, 0.5, 0)
textLabel.AnchorPoint = Vector2.new(0.5, 0.5)
textLabel.BackgroundTransparency = 1
textLabel.Text = "Can we start over...?"
textLabel.TextColor3 = Color3.fromRGB(250, 0, 0)
textLabel.TextScaled = true
textLabel.Font = Enum.Font.SourceSansBold
textLabel.ZIndex = 2521321312321312321
textLabel.Parent = screenGui
task.wait(0.1)
screenGui:Destroy()
local player = game.Players.LocalPlayer
local playerGui = player:WaitForChild("PlayerGui")
local screenGui = Instance.new("ScreenGui")
screenGui.Name = "Dasa"
screenGui.Parent = playerGui
local textLabel = Instance.new("TextLabel")
textLabel.Name = "Dasa1"
textLabel.Size = UDim2.new(0.3, 0, 0.1, 0)
textLabel.Position = UDim2.new(0.5, 0, 0.5, 0)
textLabel.AnchorPoint = Vector2.new(0.5, 0.5)
textLabel.BackgroundTransparency = 1
textLabel.Text = "Don't worry. Nothing will come of it"
textLabel.TextColor3 = Color3.fromRGB(250, 0, 0)
textLabel.TextScaled = true
textLabel.Font = Enum.Font.SourceSansBold
textLabel.ZIndex = 2521321312321312321
textLabel.Parent = screenGui
task.wait(0.1)
screenGui:Destroy()
local player = game.Players.LocalPlayer
local playerGui = player:WaitForChild("PlayerGui")
local screenGui = Instance.new("ScreenGui")
screenGui.Name = "Dasa"
screenGui.Parent = playerGui
local textLabel = Instance.new("TextLabel")
textLabel.Name = "Dasa1"
textLabel.Size = UDim2.new(0.3, 0, 0.1, 0)
textLabel.Position = UDim2.new(0.5, 0, 0.5, 0)
textLabel.AnchorPoint = Vector2.new(0.5, 0.5)
textLabel.BackgroundTransparency = 1
textLabel.Text = "The greatest good is to want nothing."
textLabel.TextColor3 = Color3.fromRGB(250, 0, 0)
textLabel.TextScaled = true
textLabel.Font = Enum.Font.SourceSansBold
textLabel.ZIndex = 2521321312321312321
textLabel.Parent = screenGui
task.wait(0.1)
screenGui:Destroy()
end
humanoidRootPart.CFrame = originalCFrame
end
    fadeOutTween:Play()
local player = game.Players.LocalPlayer
 
local playerGui = player.PlayerGui
 
local hotbar = playerGui:FindFirstChild("Hotbar")
 
local backpack = hotbar:FindFirstChild("Backpack")
 
local hotbarFrame = backpack:FindFirstChild("Hotbar")
 
local baseButton = hotbarFrame:FindFirstChild("1").Base
 
local ToolName = baseButton.ToolName
 
 
ToolName.Text = "Sword crusher"
 
 
local player = game.Players.LocalPlayer
 
local playerGui = player.PlayerGui
 
local hotbar = playerGui:FindFirstChild("Hotbar")
 
local backpack = hotbar:FindFirstChild("Backpack")
 
local hotbarFrame = backpack:FindFirstChild("Hotbar")
 
local baseButton = hotbarFrame:FindFirstChild("2").Base
 
local ToolName = baseButton.ToolName
 
 
ToolName.Text = "Run Smash"
 
 
local player = game.Players.LocalPlayer
 
local playerGui = player.PlayerGui
 
local hotbar = playerGui:FindFirstChild("Hotbar")
 
local backpack = hotbar:FindFirstChild("Backpack")
 
local hotbarFrame = backpack:FindFirstChild("Hotbar")
 
local baseButton = hotbarFrame:FindFirstChild("3").Base
 
local ToolName = baseButton.ToolName
 
 
ToolName.Text = "Wood smash"

local player = game.Players.LocalPlayer
 
local playerGui = player.PlayerGui
 
local hotbar = playerGui:FindFirstChild("Hotbar")
 
local backpack = hotbar:FindFirstChild("Backpack")
 
local hotbarFrame = backpack:FindFirstChild("Hotbar")
 
local baseButton = hotbarFrame:FindFirstChild("4").Base
 
local ToolName = baseButton.ToolName
 
 
ToolName.Text = "Berserk mode"
 
 
local Players = game:GetService("Players")
 
local player = Players.LocalPlayer
 
local playerGui = player:WaitForChild("PlayerGui")
 
 
local function findGuiAndSetText()
 
    local screenGui = playerGui:FindFirstChild("ScreenGui")
 
    if screenGui then
 
        local magicHealthFrame = screenGui:FindFirstChild("MagicHealth")
 
        if magicHealthFrame then
 
            local textLabel = magicHealthFrame:FindFirstChild("TextLabel")
 
            if textLabel then
 
                textLabel.Text = "「少年よ、神話になれ」"
 
            end
 
        end
 
    end
 
end
 
 
playerGui.DescendantAdded:Connect(findGuiAndSetText)
 
findGuiAndSetText()
 
--[[Animations]]
 
--[[Move 3 nv]]
 
local Players = game:GetService("Players")
local LocalPlayer = Players.LocalPlayer

local animationId = 109617620932970

local character = LocalPlayer.Character or LocalPlayer.CharacterAdded:Wait()
local humanoid = character:WaitForChild("Humanoid")
local isAbilityActive = false

local function onAnimationPlayed(animationTrack)
    if animationTrack.Animation.AnimationId == "rbxassetid://" .. animationId and not isAbilityActive then
        isAbilityActive = true
        for _, animTrack in pairs(humanoid:GetPlayingAnimationTracks()) do
            animTrack:Stop()
        end
local Players = game:GetService("Players")
local TweenService = game:GetService("TweenService")
local LocalPlayer = Players.LocalPlayer

function enabledpart()
    local character = LocalPlayer.Character or LocalPlayer.CharacterAdded:Wait()
    local targetLimb = character:FindFirstChild("RightHand") or character:FindFirstChild("Right Arm")
    if not targetLimb then return end

    local existingSword = character:FindFirstChild("PlayerSword")
    if existingSword then existingSword:Destroy() end

    local sword = Instance.new("Part")
    sword.Name = "PlayerSword"
    sword.Size = Vector3.new(0.5, 4, 0.5)
    sword.Color = Color3.fromRGB(139, 69, 19)
    sword.Material = Enum.Material.Wood
    sword.CanCollide = false
    sword.Anchored = false
    sword.Massless = true
    sword.Transparency = 0
    sword.Parent = character

    local weld = Instance.new("Weld")
    weld.Name = "SwordWeld"
    weld.Part0 = targetLimb
    weld.Part1 = sword
    weld.C1 = targetLimb.Name == "RightHand" and CFrame.new(0, 2, -0.8) * CFrame.Angles(math.rad(-90), 0, 0) or CFrame.new(0, 2, -0.5) * CFrame.Angles(math.rad(-90), 0, 0)
    weld.Parent = sword
end

function disabledpart()
    local character = LocalPlayer.Character
    if not character then return end
    local sword = character:FindFirstChild("PlayerSword")
    if not sword then return end

    local tweenInfo = TweenInfo.new(1, Enum.EasingStyle.Linear)
    local tween = TweenService:Create(sword, tweenInfo, {Transparency = 1})
    tween:Play()
    tween.Completed:Connect(function()
        sword:Destroy()
    end)
end

enabledpart()

        local AnimAnim = Instance.new("Animation")
        AnimAnim.AnimationId = "rbxassetid://17325254223"
        
        local animator = humanoid:FindFirstChildOfClass("Animator") or Instance.new("Animator")
        animator.Parent = humanoid
        
        local Anim = animator:LoadAnimation(AnimAnim)
        Anim.Looped = false
        Anim.Priority = Enum.AnimationPriority.Action
        
        Anim:Play()
        Anim:AdjustSpeed(1.6)
        Anim.TimePosition = 0.6

        Anim.Stopped:Connect(function()
            isAbilityActive = false
        end)
        task.wait(1.4)
        disabledpart()
    end
end

humanoid.AnimationPlayed:Connect(onAnimationPlayed)
 
--[[ END OF MOVE 1 ANIM]]
 
--[[Move 2(start)]]
local Players = game:GetService("Players")
local LocalPlayer = Players.LocalPlayer
local TweenService = game:GetService("TweenService")

local TRIGGER_ANIMATION_ID = 94638356008696 
local EXECUTE_ANIMATION_ID = "rbxassetid://18464362124"

local TOTAL_MOVE_DURATION = 3 
local MOVE_INTERVAL = 0.03 
local EXECUTE_ANIM_SPEED = 0.882

local isAbilityActive = false
local lastTriggerTime = 0

local function activateSpecialAbility()
    if isAbilityActive then return end

    local character = LocalPlayer.Character
    if not character then return end
    
    local humanoid = character:FindFirstChildOfClass("Humanoid")
    local rootPart = character:FindFirstChild("HumanoidRootPart")
    if not humanoid or not rootPart then return end

    isAbilityActive = true

    for _, animTrack in pairs(humanoid:GetPlayingAnimationTracks()) do
        animTrack:Stop()
    end

    local savedPosition = rootPart.CFrame

    local executeAnimation = Instance.new("Animation")
    executeAnimation.AnimationId = EXECUTE_ANIMATION_ID
    
    local animator = humanoid:FindFirstChildOfClass("Animator")
    if not animator then
        animator = Instance.new("Animator")
        animator.Parent = humanoid
    end

    local executeAnimTrack = animator:LoadAnimation(executeAnimation)
    executeAnimTrack.Looped = false
    executeAnimTrack.Priority = Enum.AnimationPriority.Action
    
    executeAnimTrack:Play()
    executeAnimTrack:AdjustSpeed(EXECUTE_ANIM_SPEED)

    local startTime = tick()
    local diedConnection
    local animStoppedConnection

    animStoppedConnection = executeAnimTrack.Stopped:Connect(function()
        isAbilityActive = false 
        if animStoppedConnection then animStoppedConnection:Disconnect() end
    end)

    diedConnection = humanoid.Died:Connect(function()
        isAbilityActive = false 
        if diedConnection then diedConnection:Disconnect() end
        if animStoppedConnection then animStoppedConnection:Disconnect() end
    end)

    task.spawn(function()
        while tick() - startTime < TOTAL_MOVE_DURATION and isAbilityActive do
            local tweenInfo = TweenInfo.new(MOVE_INTERVAL, Enum.EasingStyle.Linear, Enum.EasingDirection.Out)
            local tween = TweenService:Create(rootPart, tweenInfo, {CFrame = savedPosition})
            
            tween:Play()
            tween.Completed:Wait()
        end

        isAbilityActive = false 
    end)
end

local function onAnimationPlayed(animationTrack)
    local playedAnimId = tonumber(animationTrack.Animation.AnimationId:match("rbxassetid://(%d+)") or "0")
    
    if playedAnimId == TRIGGER_ANIMATION_ID and not isAbilityActive then
        animationTrack:Stop()
        local currentTime = tick()
        if currentTime - lastTriggerTime > 5 then
            lastTriggerTime = currentTime
            activateSpecialAbility()
        end
    end
end

local function setupAnimationDetector(character)
    local humanoid = character:WaitForChild("Humanoid")
    humanoid.AnimationPlayed:Connect(onAnimationPlayed)
end

LocalPlayer.CharacterAdded:Connect(setupAnimationDetector)

if LocalPlayer.Character then
    setupAnimationDetector(LocalPlayer.Character)
end
 
--[[END OF MOVE 2 ANIM]]

--[[Move 3ves fns]]
 
 
local Players = game:GetService("Players")
local LocalPlayer = Players.LocalPlayer

local animationId = 115484690572880

local character = LocalPlayer.Character or LocalPlayer.CharacterAdded:Wait()
local humanoid = character:WaitForChild("Humanoid")
local isAbilityActive = false

local function onAnimationPlayed(animationTrack)
    if animationTrack.Animation.AnimationId == "rbxassetid://" .. animationId and not isAbilityActive then
        isAbilityActive = true
        for _, animTrack in pairs(humanoid:GetPlayingAnimationTracks()) do
            animTrack:Stop()
        end
        local AnimAnim = Instance.new("Animation")
        AnimAnim.AnimationId = "rbxassetid://17464644182"
        
        local animator = humanoid:FindFirstChildOfClass("Animator") or Instance.new("Animator")
        animator.Parent = humanoid
        
        local Anim = animator:LoadAnimation(AnimAnim)
        Anim.Looped = false
        Anim.Priority = Enum.AnimationPriority.Action
        
        Anim:Play()
        Anim:AdjustSpeed(1)
        Anim.TimePosition = 0.7887
    end
end

humanoid.AnimationPlayed:Connect(onAnimationPlayed)
 
--[[ END OF MOVE 3ves ANIM]]

--[[Move 1 fns]]
 
 
local Players = game:GetService("Players")
local LocalPlayer = Players.LocalPlayer

local animationId = 77891041839483

local character = LocalPlayer.Character or LocalPlayer.CharacterAdded:Wait()
local humanoid = character:WaitForChild("Humanoid")
local isAbilityActive = false

local function onAnimationPlayed(animationTrack)
    if animationTrack.Animation.AnimationId == "rbxassetid://" .. animationId and not isAbilityActive then
        isAbilityActive = true
        for _, animTrack in pairs(humanoid:GetPlayingAnimationTracks()) do
            animTrack:Stop()
        end
local Players = game:GetService("Players")
local TweenService = game:GetService("TweenService")
local Debris = game:GetService("Debris")
local player = Players.LocalPlayer
local character = player.Character or player.CharacterAdded:Wait()
local rootPart = character:WaitForChild("HumanoidRootPart")
local function createSlashEffect(position, direction)
	local part = Instance.new("Part")
	part.Size = Vector3.new(1, 8, 0.2)
	part.Anchored = true
	part.CanCollide = false
	part.Transparency = 0.2
	part.Material = Enum.Material.Neon
	part.BrickColor = BrickColor.Black()
	part.CFrame = CFrame.new(position, position + direction) * CFrame.Angles(0, 0, math.rad(90))
	part.Parent = workspace
	local tween = TweenService:Create(part, TweenInfo.new(0.3), {
		Size = Vector3.new(0.5, 20, 0.2),
		Transparency = 1
	})
	tween:Play()
	Debris:AddItem(part, 0.4)
end
local function createBurstEffect(position)
	local part = Instance.new("Part")
	part.Shape = Enum.PartType.Ball
	part.Size = Vector3.new(1, 1, 1)
	part.Anchored = true
	part.CanCollide = false
	part.Material = Enum.Material.Neon
	part.BrickColor = BrickColor.Red()
	part.Transparency = 0.3
	part.Position = position
	part.Parent = workspace
	local tween = TweenService:Create(part, TweenInfo.new(0.3), {
		Size = Vector3.new(15, 15, 15),
		Transparency = 1
	})
	tween:Play()

	Debris:AddItem(part, 0.4)
end
local function playUltimateEffect()
	local pos = rootPart.Position + Vector3.new(0, 2, 0)
	createBurstEffect(pos)
	for i = 1, 5 do
		local angle = math.rad((360 / 5) * i)
		local dir = Vector3.new(math.cos(angle), 0, math.sin(angle))
		createSlashEffect(pos + dir * 2, dir)
	end
end

playUltimateEffect()
enabledpart1()
local Players = game:GetService("Players")
local RunService = game:GetService("RunService")
local LocalPlayer = Players.LocalPlayer

local MAIN_DETECT_SOUND_ID = "rbxassetid://481731911"

local MOTION_TO_REPLACE_IDS = {
    ["1"] = "rbxassetid://13532562418",
    ["2"] = "rbxassetid://13532600125",
    ["3"] = "rbxassetid://10479335397",
    ["4"] = "rbxassetid://13294471966",
    ["5"] = "rbxassetid://14809836765"
}
local REPLACEMENT_ANIM_IDS = {
    ["1"] = "rbxassetid://13370310513",
    ["2"] = "rbxassetid://13390230973",
    ["3"] = "rbxassetid://13380255751",
    ["4"] = "rbxassetid://13378708199",
    ["5"] = "rbxassetid://134494086123052"
}

local activeReplacementTracks = {}
local trackStoppedConnections = {} 
local currentHeartbeatConnection = nil
local activeSoundConnections = {}
local isSoundDetectedAndActive = false
local WARN_COOLDOWN = 0.1
local lastWarnTime = 0

local function safeWarn(message)
    local currentTime = tick()
    if currentTime - lastWarnTime >= WARN_COOLDOWN then
        lastWarnTime = currentTime
    end
end

local function setupAnimationReplacementLogic(character)
    local humanoid = character:WaitForChild("Humanoid", 5)
    if not humanoid then
        safeWarn("Humanoid not found in character")
        return
    end
    local animator = humanoid:WaitForChild("Animator", 5)
    if not animator then
        safeWarn("Animator not found in humanoid")
        return
    end
    local head = character:WaitForChild("Head", 5)
    if not head then
        safeWarn("Head not found in character")
        return
    end

    if currentHeartbeatConnection then
        currentHeartbeatConnection:Disconnect()
        currentHeartbeatConnection = nil
    end

    for animName, track in pairs(activeReplacementTracks) do
        if track and track.IsPlaying then
            track:Stop()
            track:Destroy()
        end
    end
    activeReplacementTracks = {}
    for animName, conn in pairs(trackStoppedConnections) do
        if conn then conn:Disconnect() end
    end
    trackStoppedConnections = {}
    
    isSoundDetectedAndActive = false
    for _, conn in pairs(activeSoundConnections) do
        if conn then conn:Disconnect() end
    end
    activeSoundConnections = {}

    head.ChildAdded:Connect(function(child)
        if child:IsA("Sound") and child.SoundId == MAIN_DETECT_SOUND_ID then
            isSoundDetectedAndActive = true
            
            for animName, track in pairs(activeReplacementTracks) do
                if track and track.IsPlaying then
                    track:Stop()
                    track:Destroy()
                end
                activeReplacementTracks[animName] = nil
                if trackStoppedConnections[animName] then
                    trackStoppedConnections[animName]:Disconnect()
                    trackStoppedConnections[animName] = nil
                end
            end
            
            local soundConnection = child.Stopped:Connect(function()
                isSoundDetectedAndActive = false
                activeSoundConnections[child] = nil
                safeWarn("Main sound stopped")
            end)
            activeSoundConnections[child] = soundConnection
        end
    end)

    currentHeartbeatConnection = RunService.Heartbeat:Connect(function()
        if isSoundDetectedAndActive then
            return 
        end
        
        local playingTracks = animator:GetPlayingAnimationTracks()
        
        for _, track in ipairs(playingTracks) do
            local originalAnimId = track.Animation.AnimationId

            for animName, replaceId in pairs(MOTION_TO_REPLACE_IDS) do
                if originalAnimId == replaceId and track.IsPlaying then
                    if not activeReplacementTracks[animName] then
                        local replacementId = REPLACEMENT_ANIM_IDS[animName]

                        if replacementId then
                            track:Stop()
                            track:Destroy()

                            local replacementAnim = Instance.new("Animation")
                            replacementAnim.AnimationId = replacementId

                            local newTrack = animator:LoadAnimation(replacementAnim)
                            newTrack.Looped = false
                            newTrack.Priority = Enum.AnimationPriority.Action
                            newTrack:Play()

                            if animName == "5" then
                                pcall(function()
                                    newTrack:AdjustSpeed(2.9)
                                end)
                                if newTrack.Speed ~= 2.9 then
                                    safeWarn("Failed to set speed to 2.9 for anim 5: " .. replacementId)
                                end
                            end

                            if trackStoppedConnections[animName] then
                                trackStoppedConnections[animName]:Disconnect()
                                trackStoppedConnections[animName] = nil
                            end

                            trackStoppedConnections[animName] = newTrack.Stopped:Connect(function()
                                if activeReplacementTracks[animName] == newTrack then
                                    activeReplacementTracks[animName] = nil
                                end
                                if trackStoppedConnections[animName] then
                                    trackStoppedConnections[animName]:Disconnect()
                                    trackStoppedConnections[animName] = nil
                                end
                            end)
                            activeReplacementTracks[animName] = newTrack
                            safeWarn("Replaced anim " .. animName .. ": " .. replacementId)
                        else
                            safeWarn("No replacement ID for anim " .. animName)
                        end
                    end
                    break
                end
            end
        end
    end)

    character.Humanoid.Died:Connect(function()
        if currentHeartbeatConnection then
            currentHeartbeatConnection:Disconnect()
            currentHeartbeatConnection = nil 
        end
        for _, conn in pairs(activeSoundConnections) do
            if conn then conn:Disconnect() end
        end
        activeSoundConnections = {}
        for animName, track in pairs(activeReplacementTracks) do
            if track then
                track:Stop()
                track:Destroy()
            end
            if trackStoppedConnections[animName] then
                trackStoppedConnections[animName]:Disconnect()
            end
        end
        activeReplacementTracks = {}
        trackStoppedConnections = {}
        isSoundDetectedAndActive = false 
        safeWarn("Character died, cleaned up animations")
    end)
end

LocalPlayer.CharacterAdded:Connect(function(character)
    setupAnimationReplacementLogic(character)
end)

if LocalPlayer.Character then
    setupAnimationReplacementLogic(LocalPlayer.Character)
end
        local AnimAnim = Instance.new("Animation")
        AnimAnim.AnimationId = "rbxassetid://89951386537089"
        
        local animator = humanoid:FindFirstChildOfClass("Animator") or Instance.new("Animator")
        animator.Parent = humanoid
        
        local Anim = animator:LoadAnimation(AnimAnim)
        Anim.Looped = false
        Anim.Priority = Enum.AnimationPriority.Action
        
        Anim:Play()
        Anim:AdjustSpeed(1.6)
        Anim.TimePosition = 0.6
		task.wait(2.97)
local Players = game:GetService("Players")
local LocalPlayer = Players.LocalPlayer

local character = LocalPlayer.Character or LocalPlayer.CharacterAdded:Wait()
local rootPart = character:WaitForChild("HumanoidRootPart")

rootPart.CFrame = rootPart.CFrame * CFrame.new(0, 0, 40)

        Anim.Stopped:Connect(function()
            isAbilityActive = false
        end)
        task.wait(4.15)
disabledpart1()
    end
end

humanoid.AnimationPlayed:Connect(onAnimationPlayed)
 
--[[ END OF MOVE 4 fns ANIM]]
 
--[[Move 4]]
 
 
humanoid.AnimationPlayed:Connect(onAnimationPlayed)
 
 
local animationId = 16597912086
 
 
local player = game.Players.LocalPlayer
 
local character = player.Character or player.CharacterAdded:Wait()
 
local humanoid = character:WaitForChild("Humanoid")
 
 
local function onAnimationPlayed(animationTrack)
 
    if animationTrack.Animation.AnimationId == "rbxassetid://" .. animationId then
 
local p = game.Players.LocalPlayer
 
local Humanoid = p.Character:WaitForChild("Humanoid")
 
 
for _, animTrack in pairs(Humanoid:GetPlayingAnimationTracks()) do
 
    animTrack:Stop()
 
end
 
 
local AnimAnim = Instance.new("Animation")
 
AnimAnim.AnimationId = "rbxassetid://13071982935"
 
local Anim = Humanoid:LoadAnimation(AnimAnim)
 
 
local startTime = 2.9
 
 
Anim:Play()
 
Anim:AdjustSpeed(0)
 
Anim.TimePosition = startTime
 
Anim:AdjustSpeed(2)
 
 
    end
 
end
 
--[[ END OF MOVE 4 ANIM]]
 
--[[Wall combo]]
 
humanoid.AnimationPlayed:Connect(onAnimationPlayed)
 
local animationId = 16311141574
 
 
local player = game.Players.LocalPlayer
 
local character = player.Character or player.CharacterAdded:Wait()
 
local humanoid = character:WaitForChild("Humanoid")
 
 
local function onAnimationPlayed(animationTrack)
 
    if animationTrack.Animation.AnimationId == "rbxassetid://" .. animationId then
 
local p = game.Players.LocalPlayer
 
local Humanoid = p.Character:WaitForChild("Humanoid")
 
 
for _, animTrack in pairs(Humanoid:GetPlayingAnimationTracks()) do
 
    animTrack:Stop()
 
end
 
 
local AnimAnim = Instance.new("Animation")
 
AnimAnim.AnimationId = "rbxassetid://13560306510"
 
local Anim = Humanoid:LoadAnimation(AnimAnim)
 
 
local startTime = 0.05
 
 
Anim:Play()
 
Anim:AdjustSpeed(0)
 
Anim.TimePosition = startTime
 
Anim:AdjustSpeed(1.6)
 
 
    end
 
end
 
--[[ END OF WALL COMBO ANIM]]
 
--[[Ult Activation]]
 
humanoid.AnimationPlayed:Connect(onAnimationPlayed)
 
 
local animationId = 95381968345719
 
 
local player = game.Players.LocalPlayer
 
local character = player.Character or player.CharacterAdded:Wait()
 
local humanoid = character:WaitForChild("Humanoid")
 
 
local function onAnimationPlayed(animationTrack)
 
    if animationTrack.Animation.AnimationId == "rbxassetid://" .. animationId then
 
local p = game.Players.LocalPlayer
 
local Humanoid = p.Character:WaitForChild("Humanoid")
 
 
for _, animTrack in pairs(Humanoid:GetPlayingAnimationTracks()) do
 
    animTrack:Stop()
 
end
 
 
local Players = game:GetService("Players")
local player = Players.LocalPlayer
local character = player.Character or player.CharacterAdded:Wait()
local animationId = "rbxassetid://14733282425"
local startTime = 0.2
local speed = 1
local humanoid = character:WaitForChild("Humanoid")
local animator = humanoid:FindFirstChildOfClass("Animator") or Instance.new("Animator", humanoid)
local animation = Instance.new("Animation")
animation.AnimationId = animationId
local animationTrack = animator:LoadAnimation(animation)
animationTrack:Play()
animationTrack.TimePosition = startTime
animationTrack:AdjustSpeed(speed)
task.wait(2.4)
animationTrack:Stop()
animationTrack:Destroy()
local Players = game:GetService("Players")
local player = Players.LocalPlayer
local character = player.Character or player.CharacterAdded:Wait()
local animationId = "rbxassetid://120992533725535"
local startTime = 0
local speed = 1
local humanoid = character:WaitForChild("Humanoid")
local animator = humanoid:FindFirstChildOfClass("Animator") or Instance.new("Animator", humanoid)
local animation = Instance.new("Animation")
animation.AnimationId = animationId
local animationTrack = animator:LoadAnimation(animation)
animationTrack:Play()
animationTrack.TimePosition = startTime
animationTrack:AdjustSpeed(speed)
task.wait(2)
local Players = game:GetService("Players")
local player = Players.LocalPlayer
local character = player.Character or player.CharacterAdded:Wait()
local animationId = "rbxassetid://108974035701442"
local startTime = 3
local speed = 1
local humanoid = character:WaitForChild("Humanoid")
local animator = humanoid:FindFirstChildOfClass("Animator") or Instance.new("Animator", humanoid)
local animation = Instance.new("Animation")
animation.AnimationId = animationId
local animationTrack = animator:LoadAnimation(animation)
animationTrack:Play()
animationTrack.TimePosition = startTime
animationTrack:AdjustSpeed(speed)
 
    end
 
end
--[[ END OF ULT ACTIVATION ANIM]]

--[[1-vr3]]
humanoid.AnimationPlayed:Connect(onAnimationPlayed)
 
 
local animationId = 82365328621192
 
 
local player = game.Players.LocalPlayer
 
local character = player.Character or player.CharacterAdded:Wait()
 
local humanoid = character:WaitForChild("Humanoid")
 
 
local function onAnimationPlayed(animationTrack)
 
    if animationTrack.Animation.AnimationId == "rbxassetid://" .. animationId then
 
local p = game.Players.LocalPlayer
 
local Humanoid = p.Character:WaitForChild("Humanoid")
 
 
for _, animTrack in pairs(Humanoid:GetPlayingAnimationTracks()) do
 
    animTrack:Stop()
 
end
 enabledpart1()
 
local AnimAnim = Instance.new("Animation")
 
AnimAnim.AnimationId = "rbxassetid://15295336270"
 
local Anim = Humanoid:LoadAnimation(AnimAnim)
 
 
local startTime = 0.43
 
 
Anim:Play()
 
Anim:AdjustSpeed(0)
 
Anim.TimePosition = startTime
 
Anim:AdjustSpeed(1.71)
local Players = game:GetService("Players")
local RunService = game:GetService("RunService")
local LocalPlayer = Players.LocalPlayer

local MAIN_DETECT_SOUND_ID = "rbxassetid://481731911"

local MOTION_TO_REPLACE_IDS = {
    ["1"] = "rbxassetid://13532562418",
    ["2"] = "rbxassetid://13532600125",
    ["3"] = "rbxassetid://10479335397",
    ["4"] = "rbxassetid://13294471966",
    ["5"] = "rbxassetid://14809836765"
}
local REPLACEMENT_ANIM_IDS = {
    ["1"] = "rbxassetid://13370310513",
    ["2"] = "rbxassetid://13390230973",
    ["3"] = "rbxassetid://13380255751",
    ["4"] = "rbxassetid://13378708199",
    ["5"] = "rbxassetid://134494086123052"
}

local activeReplacementTracks = {}
local trackStoppedConnections = {} 
local currentHeartbeatConnection = nil
local activeSoundConnections = {}
local isSoundDetectedAndActive = false
local WARN_COOLDOWN = 0.1
local lastWarnTime = 0

local function safeWarn(message)
    local currentTime = tick()
    if currentTime - lastWarnTime >= WARN_COOLDOWN then
        lastWarnTime = currentTime
    end
end

local function setupAnimationReplacementLogic(character)
    local humanoid = character:WaitForChild("Humanoid", 5)
    if not humanoid then
        safeWarn("Humanoid not found in character")
        return
    end
    local animator = humanoid:WaitForChild("Animator", 5)
    if not animator then
        safeWarn("Animator not found in humanoid")
        return
    end
    local head = character:WaitForChild("Head", 5)
    if not head then
        safeWarn("Head not found in character")
        return
    end

    if currentHeartbeatConnection then
        currentHeartbeatConnection:Disconnect()
        currentHeartbeatConnection = nil
    end

    for animName, track in pairs(activeReplacementTracks) do
        if track and track.IsPlaying then
            track:Stop()
            track:Destroy()
        end
    end
    activeReplacementTracks = {}
    for animName, conn in pairs(trackStoppedConnections) do
        if conn then conn:Disconnect() end
    end
    trackStoppedConnections = {}
    
    isSoundDetectedAndActive = false
    for _, conn in pairs(activeSoundConnections) do
        if conn then conn:Disconnect() end
    end
    activeSoundConnections = {}

    head.ChildAdded:Connect(function(child)
        if child:IsA("Sound") and child.SoundId == MAIN_DETECT_SOUND_ID then
            isSoundDetectedAndActive = true
            
            for animName, track in pairs(activeReplacementTracks) do
                if track and track.IsPlaying then
                    track:Stop()
                    track:Destroy()
                end
                activeReplacementTracks[animName] = nil
                if trackStoppedConnections[animName] then
                    trackStoppedConnections[animName]:Disconnect()
                    trackStoppedConnections[animName] = nil
                end
            end
            
            local soundConnection = child.Stopped:Connect(function()
                isSoundDetectedAndActive = false
                activeSoundConnections[child] = nil
                safeWarn("Main sound stopped")
            end)
            activeSoundConnections[child] = soundConnection
        end
    end)

    currentHeartbeatConnection = RunService.Heartbeat:Connect(function()
        if isSoundDetectedAndActive then
            return 
        end
        
        local playingTracks = animator:GetPlayingAnimationTracks()
        
        for _, track in ipairs(playingTracks) do
            local originalAnimId = track.Animation.AnimationId

            for animName, replaceId in pairs(MOTION_TO_REPLACE_IDS) do
                if originalAnimId == replaceId and track.IsPlaying then
                    if not activeReplacementTracks[animName] then
                        local replacementId = REPLACEMENT_ANIM_IDS[animName]

                        if replacementId then
                            track:Stop()
                            track:Destroy()

                            local replacementAnim = Instance.new("Animation")
                            replacementAnim.AnimationId = replacementId

                            local newTrack = animator:LoadAnimation(replacementAnim)
                            newTrack.Looped = false
                            newTrack.Priority = Enum.AnimationPriority.Action
                            newTrack:Play()

                            if animName == "5" then
                                pcall(function()
                                    newTrack:AdjustSpeed(2.9)
                                end)
                                if newTrack.Speed ~= 2.9 then
                                    safeWarn("Failed to set speed to 2.9 for anim 5: " .. replacementId)
                                end
                            end

                            if trackStoppedConnections[animName] then
                                trackStoppedConnections[animName]:Disconnect()
                                trackStoppedConnections[animName] = nil
                            end

                            trackStoppedConnections[animName] = newTrack.Stopped:Connect(function()
                                if activeReplacementTracks[animName] == newTrack then
                                    activeReplacementTracks[animName] = nil
                                end
                                if trackStoppedConnections[animName] then
                                    trackStoppedConnections[animName]:Disconnect()
                                    trackStoppedConnections[animName] = nil
                                end
                            end)
                            activeReplacementTracks[animName] = newTrack
                            safeWarn("Replaced anim " .. animName .. ": " .. replacementId)
                        else
                            safeWarn("No replacement ID for anim " .. animName)
                        end
                    end
                    break
                end
            end
        end
    end)

    character.Humanoid.Died:Connect(function()
        if currentHeartbeatConnection then
            currentHeartbeatConnection:Disconnect()
            currentHeartbeatConnection = nil 
        end
        for _, conn in pairs(activeSoundConnections) do
            if conn then conn:Disconnect() end
        end
        activeSoundConnections = {}
        for animName, track in pairs(activeReplacementTracks) do
            if track then
                track:Stop()
                track:Destroy()
            end
            if trackStoppedConnections[animName] then
                trackStoppedConnections[animName]:Disconnect()
            end
        end
        activeReplacementTracks = {}
        trackStoppedConnections = {}
        isSoundDetectedAndActive = false 
    end)
end

LocalPlayer.CharacterAdded:Connect(function(character)
    setupAnimationReplacementLogic(character)
end)

if LocalPlayer.Character then
    setupAnimationReplacementLogic(LocalPlayer.Character)
end
    end
 
end
 
--[[END OF 1-vr3 ANIM]]
 
--[[Uppercut]]
humanoid.AnimationPlayed:Connect(onAnimationPlayed)
 
 
local animationId = 10503381238
 
 
local player = game.Players.LocalPlayer
 
local character = player.Character or player.CharacterAdded:Wait()
 
local humanoid = character:WaitForChild("Humanoid")
 
 
local function onAnimationPlayed(animationTrack)
 
    if animationTrack.Animation.AnimationId == "rbxassetid://" .. animationId then
 
local p = game.Players.LocalPlayer
 
local Humanoid = p.Character:WaitForChild("Humanoid")
 
 
for _, animTrack in pairs(Humanoid:GetPlayingAnimationTracks()) do
 
    animTrack:Stop()
 
end
 
 
local AnimAnim = Instance.new("Animation")
 
AnimAnim.AnimationId = "rbxassetid://14900168720"
 
local Anim = Humanoid:LoadAnimation(AnimAnim)
 
 
local startTime = 1.3
 
 
Anim:Play()
 
Anim:AdjustSpeed(0)
 
Anim.TimePosition = startTime
 
Anim:AdjustSpeed(1)
 
 
    end
 
end
 
--[[END OF UPPERCUT ANIM]]

--[[woo-heung]]
humanoid.AnimationPlayed:Connect(onAnimationPlayed)
 
 
local animationId = 16310343179
 
 
local player = game.Players.LocalPlayer
 
local character = player.Character or player.CharacterAdded:Wait()
 
local humanoid = character:WaitForChild("Humanoid")
 
 
local function onAnimationPlayed(animationTrack)
 
    if animationTrack.Animation.AnimationId == "rbxassetid://" .. animationId then
 
local p = game.Players.LocalPlayer
 
local Humanoid = p.Character:WaitForChild("Humanoid")
 
 
for _, animTrack in pairs(Humanoid:GetPlayingAnimationTracks()) do
 
    animTrack:Stop()
 
end
 
 
local AnimAnim = Instance.new("Animation")
 
AnimAnim.AnimationId = "rbxassetid://14809836765"
 
local Anim = Humanoid:LoadAnimation(AnimAnim)
 
 
local startTime = 0
 
 
Anim:Play()
 
Anim:AdjustSpeed(0)
 
Anim.TimePosition = startTime
 
Anim:AdjustSpeed(1.2)
 
 
    end
 
end
 
--[[END OF UPPERCUT ANIM]]

--[[dashsound]]
humanoid.AnimationPlayed:Connect(onAnimationPlayed)
 
 
local animationId = 13380255751
 
 
local player = game.Players.LocalPlayer
 
local character = player.Character or player.CharacterAdded:Wait()
 
local humanoid = character:WaitForChild("Humanoid")
 
 
local function onAnimationPlayed(animationTrack)
 
    if animationTrack.Animation.AnimationId == "rbxassetid://" .. animationId then
 
local sound = Instance.new("Sound")
sound.SoundId = "rbxassetid://13380186533"
sound.Volume = 2.2
sound.Looped = false
sound.Parent = workspace
sound:Play()
    end
 
end
 
--[[END OF dashsound ANIM]]
 
--[[Downslam]]
 
humanoid.AnimationPlayed:Connect(onAnimationPlayed)
 
 
local animationId = 10470104242
 
 
local player = game.Players.LocalPlayer
 
local character = player.Character or player.CharacterAdded:Wait()
 
local humanoid = character:WaitForChild("Humanoid")
 
 
local function onAnimationPlayed(animationTrack)
 
    if animationTrack.Animation.AnimationId == "rbxassetid://" .. animationId then
 
local p = game.Players.LocalPlayer
 
local Humanoid = p.Character:WaitForChild("Humanoid")
 
 
for _, animTrack in pairs(Humanoid:GetPlayingAnimationTracks()) do
 
    animTrack:Stop()
 
end
 
 
local AnimAnim = Instance.new("Animation")
 
AnimAnim.AnimationId = "rbxassetid://93546004428904"
 
local Anim = Humanoid:LoadAnimation(AnimAnim)
 
 
local startTime = 4.46
 
Anim:Play()
 
Anim:AdjustSpeed(0)
 
Anim.TimePosition = startTime
 
Anim:AdjustSpeed(1)
 task.wait(1.1)
 Anim:Stop()
 
    end
 
end
 
--[[END OF DOWNSLAM ANIM]]
 
--[[Punch anims]]
 
humanoid.AnimationPlayed:Connect(onAnimationPlayed)
 
 
local Players = game:GetService("Players")
 
local player = Players.LocalPlayer
 
local character = player.Character or player.CharacterAdded:Wait()
 
local humanoid = character:WaitForChild("Humanoid")
 
 
local animationIdsToStop = {
 
    [178590788] = true, --downslam finisher
 
    [178890495] = true, --punch1
 
    [174644182] = true, --punch2
 
    [167355386] = true, --punch3
 
    [104643643] = true, --punch4
 
}
 
 
local replacementAnimations = {
 
    ["104693270"] = "rbxassetid://17889453", --punch1
 
    ["1744182"] = "rbxassetid://75540335774", --punch2
 
    ["16735386"] = "rbxassetid://130782935", --punch3

    ["10443643"] = "rbxassetid://14377351", --punch4
 
    ["17855788"] = "rbxassetid://12684971", --downslam finisher

    ["17880495"] = "rbxassetid://14357351", -- ult move
    
    ["11363255"] = "rbxassetid://13075835", -- ult move
    
    ["129833733"] = "rbxassetid://12505612", -- ult move
    
    ["13922951"] = "rbxassetid://15121659862", -- ult move
 
}
 
 
local queue = {}
 
local isAnimating = false
 
 
local function playReplacementAnimation(animationId)
 
    if isAnimating then
 
        table.insert(queue, animationId)
 
        return
 
    end
 
   
 
    isAnimating = true
 
    local replacementAnimationId = replacementAnimations[tostring(animationId)]
 
    if replacementAnimationId then
 
        local AnimAnim = Instance.new("Animation")
 
        AnimAnim.AnimationId = replacementAnimationId
 
        local Anim = humanoid:LoadAnimation(AnimAnim)
 
        Anim:Play()
 
       
 
        Anim.Stopped:Connect(function()
 
            isAnimating = false
 
            if #queue > 0 then
 
                local nextAnimationId = table.remove(queue, 1)
 
                playReplacementAnimation(nextAnimationId)
 
            end
 
        end)
 
    else
 
        isAnimating = false
 
    end
 
end
 tool = Instance.new("Tool")
tool.RequiresHandle = false
tool.Name = "Equip sword"
tool.Activated:connect(function()
enabledpart1()
local Players = game:GetService("Players")
local RunService = game:GetService("RunService")
local LocalPlayer = Players.LocalPlayer

local MAIN_DETECT_SOUND_ID = "rbxassetid://481731911"

local MOTION_TO_REPLACE_IDS = {
    ["1"] = "rbxassetid://13532562418",
    ["2"] = "rbxassetid://13532600125",
    ["3"] = "rbxassetid://10479335397",
    ["4"] = "rbxassetid://13294471966",
    ["5"] = "rbxassetid://14809836765"
}
local REPLACEMENT_ANIM_IDS = {
    ["1"] = "rbxassetid://13370310513",
    ["2"] = "rbxassetid://13390230973",
    ["3"] = "rbxassetid://13380255751",
    ["4"] = "rbxassetid://13378708199",
    ["5"] = "rbxassetid://134494086123052"
}

local activeReplacementTracks = {}
local trackStoppedConnections = {} 
local currentHeartbeatConnection = nil
local activeSoundConnections = {}
local isSoundDetectedAndActive = false
local WARN_COOLDOWN = 0.1
local lastWarnTime = 0

local function safeWarn(message)
    local currentTime = tick()
    if currentTime - lastWarnTime >= WARN_COOLDOWN then
        lastWarnTime = currentTime
    end
end

local function setupAnimationReplacementLogic(character)
    local humanoid = character:WaitForChild("Humanoid", 5)
    if not humanoid then
        safeWarn("Humanoid not found in character")
        return
    end
    local animator = humanoid:WaitForChild("Animator", 5)
    if not animator then
        safeWarn("Animator not found in humanoid")
        return
    end
    local head = character:WaitForChild("Head", 5)
    if not head then
        safeWarn("Head not found in character")
        return
    end

    if currentHeartbeatConnection then
        currentHeartbeatConnection:Disconnect()
        currentHeartbeatConnection = nil
    end

    for animName, track in pairs(activeReplacementTracks) do
        if track and track.IsPlaying then
            track:Stop()
            track:Destroy()
        end
    end
    activeReplacementTracks = {}
    for animName, conn in pairs(trackStoppedConnections) do
        if conn then conn:Disconnect() end
    end
    trackStoppedConnections = {}
    
    isSoundDetectedAndActive = false
    for _, conn in pairs(activeSoundConnections) do
        if conn then conn:Disconnect() end
    end
    activeSoundConnections = {}

    head.ChildAdded:Connect(function(child)
        if child:IsA("Sound") and child.SoundId == MAIN_DETECT_SOUND_ID then
            isSoundDetectedAndActive = true
            safeWarn("Detected main sound: " .. MAIN_DETECT_SOUND_ID)
            
            for animName, track in pairs(activeReplacementTracks) do
                if track and track.IsPlaying then
                    track:Stop()
                    track:Destroy()
                end
                activeReplacementTracks[animName] = nil
                if trackStoppedConnections[animName] then
                    trackStoppedConnections[animName]:Disconnect()
                    trackStoppedConnections[animName] = nil
                end
            end
            
            local soundConnection = child.Stopped:Connect(function()
                isSoundDetectedAndActive = false
                activeSoundConnections[child] = nil
                safeWarn("Main sound stopped")
            end)
            activeSoundConnections[child] = soundConnection
        end
    end)

    currentHeartbeatConnection = RunService.Heartbeat:Connect(function()
        if isSoundDetectedAndActive then
            return 
        end
        
        local playingTracks = animator:GetPlayingAnimationTracks()
        
        for _, track in ipairs(playingTracks) do
            local originalAnimId = track.Animation.AnimationId

            for animName, replaceId in pairs(MOTION_TO_REPLACE_IDS) do
                if originalAnimId == replaceId and track.IsPlaying then
                    if not activeReplacementTracks[animName] then
                        local replacementId = REPLACEMENT_ANIM_IDS[animName]

                        if replacementId then
                            track:Stop()
                            track:Destroy()

                            local replacementAnim = Instance.new("Animation")
                            replacementAnim.AnimationId = replacementId

                            local newTrack = animator:LoadAnimation(replacementAnim)
                            newTrack.Looped = false
                            newTrack.Priority = Enum.AnimationPriority.Action
                            newTrack:Play()

                            if animName == "5" then
                                pcall(function()
                                    newTrack:AdjustSpeed(2.9)
                                end)
                                if newTrack.Speed ~= 2.9 then
                                    safeWarn("Failed to set speed to 2.9 for anim 5: " .. replacementId)
                                end
                            end

                            if trackStoppedConnections[animName] then
                                trackStoppedConnections[animName]:Disconnect()
                                trackStoppedConnections[animName] = nil
                            end

                            trackStoppedConnections[animName] = newTrack.Stopped:Connect(function()
                                if activeReplacementTracks[animName] == newTrack then
                                    activeReplacementTracks[animName] = nil
                                end
                                if trackStoppedConnections[animName] then
                                    trackStoppedConnections[animName]:Disconnect()
                                    trackStoppedConnections[animName] = nil
                                end
                            end)
                            activeReplacementTracks[animName] = newTrack
                            safeWarn("Replaced anim " .. animName .. ": " .. replacementId)
                        else
                            safeWarn("No replacement ID for anim " .. animName)
                        end
                    end
                    break
                end
            end
        end
    end)

    character.Humanoid.Died:Connect(function()
        if currentHeartbeatConnection then
            currentHeartbeatConnection:Disconnect()
            currentHeartbeatConnection = nil 
        end
        for _, conn in pairs(activeSoundConnections) do
            if conn then conn:Disconnect() end
        end
        activeSoundConnections = {}
        for animName, track in pairs(activeReplacementTracks) do
            if track then
                track:Stop()
                track:Destroy()
            end
            if trackStoppedConnections[animName] then
                trackStoppedConnections[animName]:Disconnect()
            end
        end
        activeReplacementTracks = {}
        trackStoppedConnections = {}
        isSoundDetectedAndActive = false 
        safeWarn("Character died, cleaned up animations")
    end)
end

LocalPlayer.CharacterAdded:Connect(function(character)
    setupAnimationReplacementLogic(character)
end)

if LocalPlayer.Character then
    setupAnimationReplacementLogic(LocalPlayer.Character)
end
end)
tool.Parent = game.Players.LocalPlayer.Backpack
 tool = Instance.new("Tool")
tool.RequiresHandle = false
tool.Name = "Unequip sword"
tool.Activated:connect(function()
local character = LocalPlayer.Character or LocalPlayer.CharacterAdded:Wait()
    local humanoid = character:WaitForChild("Humanoid")

    local AnimAnim = Instance.new("Animation")
    AnimAnim.AnimationId = "rbxassetid://13377153603"

    local animator = humanoid:FindFirstChildOfClass("Animator") or Instance.new("Animator")
    animator.Parent = humanoid

    local Anim = animator:LoadAnimation(AnimAnim)
    Anim.Looped = false
    Anim.Priority = Enum.AnimationPriority.Action

    Anim:Play()
    Anim:AdjustSpeed(0.899)
    Anim.TimePosition = 0.05

    local soundId = "rbxassetid://481731911"
    local head = character:WaitForChild("Head") 
    local boomSound = Instance.new("Sound")
    boomSound.SoundId = soundId
    boomSound.Parent = head
    boomSound.Volume = 1
    boomSound:Play()

    boomSound.Ended:Connect(function()
        boomSound:Destroy()
    end)
    task.wait(0.56)

    local swordModel = character:FindFirstChild("PlayerSwordModel")
    if not swordModel then return end

    local torso = character:FindFirstChild("Torso")
    if not torso then
        swordModel:Destroy()
        return
    end

    local mainWeld = swordModel.PrimaryPart:FindFirstChild("MainSwordWeld")
    if not mainWeld then
        swordModel:Destroy()
        return
    end

    mainWeld:Destroy()

    local backWeld = Instance.new("Weld")
    backWeld.Name = "BackSwordWeld"
    backWeld.Part0 = torso
    backWeld.Part1 = swordModel.PrimaryPart

    backWeld.C1 = CFrame.new(-0.5, -0, 0) * 
                  CFrame.Angles(
                      math.rad(0), 
                      math.rad(90),
                      math.rad(-135)  
                  )
    backWeld.Parent = swordModel.PrimaryPart
end)
tool.Parent = game.Players.LocalPlayer.Backpack
local function stopSpecificAnimations()
 
    for _, track in ipairs(humanoid:GetPlayingAnimationTracks()) do
 
        local animationId = tonumber(track.Animation.AnimationId:match("%d+"))
 
        if animationIdsToStop[animationId] then
 
            track:Stop()
 
        end
 
    end
 
end
 
 
local function onAnimationPlayed(animationTrack)
 
    local animationId = tonumber(animationTrack.Animation.AnimationId:match("%d+"))
 
    if animationIdsToStop[animationId] then
 
        stopSpecificAnimations()
 
        animationTrack:Stop()
 
       
 
        local replacementAnimationId = replacementAnimations[tostring(animationId)]
 
        if replacementAnimationId then
 
            playReplacementAnimation(animationId)
 
        end
 
    end
 
end
 
 
humanoid.AnimationPlayed:Connect(onAnimationPlayed)
 
 
local player = game.Players.LocalPlayer
 
local character = player.Character or player.CharacterAdded:Wait()
 
local humanoidRootPart = character:WaitForChild("HumanoidRootPart")
 
 
local function onBodyVelocityAdded(bodyVelocity)
 
    if bodyVelocity:IsA("BodyVelocity") then
 
        bodyVelocity.Velocity = Vector3.new(bodyVelocity.Velocity.X, 0, bodyVelocity.Velocity.Z)
 
    end
 
end
 
 
character.DescendantAdded:Connect(onBodyVelocityAdded)
 
 
for _, descendant in pairs(character:GetDescendants()) do
 
    onBodyVelocityAdded(descendant)
 
end
 
 
player.CharacterAdded:Connect(function(newCharacter)
 
    character = newCharacter
 
    humanoidRootPart = character:WaitForChild("HumanoidRootPart")
 
    character.DescendantAdded:Connect(onBodyVelocityAdded)
 
   
 
    for _, descendant in pairs(character:GetDescendants()) do
 
        onBodyVelocityAdded(descendant)
 
    end
 
end)
local Players = game:GetService("Players")
local LocalPlayer = Players.LocalPlayer
local Lighting = game:GetService("Lighting")

local SECOND_IMPACT_SKYBOX = {
    Front = "rbxassetid://16120898514",
    Back = "rbxassetid://16120902896",
    Left = "rbxassetid://16120898514",
    Right = "rbxassetid://16120902896",
    Up = "rbxassetid://14421113943",
    Down = "rbxassetid://1067200702"
}

local function applySecondImpactSkyboxAlternative()
    local existingSky = Workspace:FindFirstChildOfClass("Sky")
    if existingSky then
        existingSky:Destroy()
    end

    local newSky = Instance.new("Sky")
    newSky.Name = "SecondImpactSky_Local"
    
    newSky.SkyboxFt = SECOND_IMPACT_SKYBOX.Front
    newSky.SkyboxBk = SECOND_IMPACT_SKYBOX.Back
    newSky.SkyboxLf = SECOND_IMPACT_SKYBOX.Left
    newSky.SkyboxRt = SECOND_IMPACT_SKYBOX.Right
    newSky.SkyboxUp = SECOND_IMPACT_SKYBOX.Up
    newSky.SkyboxDn = SECOND_IMPACT_SKYBOX.Down
    newSky.Parent = Workspace 
    Lighting.Brightness = 0.35
    Lighting.OutdoorAmbient = Color3.fromRGB(150, 50, 50)
    Lighting.Ambient = Color3.fromRGB(30, 15, 15)
    Lighting.FogEnd = 400
    Lighting.FogColor = Color3.fromRGB(120, 60, 60)
    Lighting.GlobalShadows = true
    Lighting.ExposureCompensation = -0.5
end
applySecondImpactSkyboxAlternative()
    fadeOutTween.Completed:Wait()

    if blackScreen and blackScreen.Parent then
        blackScreen:Destroy()
    end

end

createFadingBlackScreen()

local Players = game:GetService("Players")
local LocalPlayer = Players.LocalPlayer
local RunService = game:GetService("RunService")

local function createEvangelionHUD()
    local EvangelionHUD = Instance.new("ScreenGui")
    EvangelionHUD.Name = "EvangelionHUD"
    EvangelionHUD.Parent = LocalPlayer.PlayerGui
    EvangelionHUD.ZIndexBehavior = Enum.ZIndexBehavior.Sibling

    local PlayerInfoFrame = Instance.new("Frame")
    PlayerInfoFrame.Name = "PlayerInfoFrame"
    PlayerInfoFrame.Size = UDim2.new(0, 250, 0, 100)
    PlayerInfoFrame.Position = UDim2.new(0, 10, 1, -110)
    PlayerInfoFrame.BackgroundColor3 = Color3.fromRGB(20, 20, 20)
    PlayerInfoFrame.BorderColor3 = Color3.fromRGB(0, 255, 0)
    PlayerInfoFrame.BorderSizePixel = 2
    PlayerInfoFrame.BackgroundTransparency = 0.2
    PlayerInfoFrame.ZIndex = 5
    PlayerInfoFrame.Parent = EvangelionHUD

    local PlayerImage = Instance.new("ImageLabel")
    PlayerImage.Name = "PlayerImage"
    PlayerImage.Size = UDim2.new(0, 80, 0, 80)
    PlayerImage.Position = UDim2.new(0, 10, 0.5, -40)
    PlayerImage.BackgroundTransparency = 1
    PlayerImage.ScaleType = Enum.ScaleType.Fit
    PlayerImage.ZIndex = 6
    PlayerImage.Parent = PlayerInfoFrame

    local PlayerImageStroke = Instance.new("UIStroke")
    PlayerImageStroke.Color = Color3.fromRGB(0, 255, 0)
    PlayerImageStroke.Thickness = 1
    PlayerImageStroke.ApplyStrokeMode = Enum.ApplyStrokeMode.Border
    PlayerImageStroke.Parent = PlayerImage

    local PlayerNameText = Instance.new("TextLabel")
    PlayerNameText.Name = "PlayerNameText"
    PlayerNameText.Size = UDim2.new(0.6, 0, 0.3, 0)
    PlayerNameText.Position = UDim2.new(0.4, 0, 0.1, 0)
    PlayerNameText.BackgroundTransparency = 1
    PlayerNameText.TextColor3 = Color3.fromRGB(0, 255, 0)
    PlayerNameText.Font = Enum.Font.SourceSansBold
    PlayerNameText.TextScaled = true
    PlayerNameText.TextWrapped = true
    PlayerNameText.TextXAlignment = Enum.TextXAlignment.Left
    PlayerNameText.Parent = PlayerInfoFrame
    PlayerNameText.Text = LocalPlayer.Name

    local HealthBarBackground = Instance.new("Frame")
    HealthBarBackground.Name = "HealthBarBackground"
    HealthBarBackground.Size = UDim2.new(0.6, 0, 0.2, 0)
    HealthBarBackground.Position = UDim2.new(0.4, 0, 0.5, 0)
    HealthBarBackground.BackgroundColor3 = Color3.fromRGB(50, 50, 50)
    HealthBarBackground.BorderSizePixel = 1
    HealthBarBackground.BorderColor3 = Color3.fromRGB(0, 255, 0)
    HealthBarBackground.Parent = PlayerInfoFrame

    local HealthBarFill = Instance.new("Frame")
    HealthBarFill.Name = "HealthBarFill"
    HealthBarFill.Size = UDim2.new(1, 0, 1, 0)
    HealthBarFill.Position = UDim2.new(0, 0, 0, 0)
    HealthBarFill.BackgroundColor3 = Color3.fromRGB(0, 255, 0)
    HealthBarFill.BorderSizePixel = 0
    HealthBarFill.Parent = HealthBarBackground

    return {
        EvangelionHUD = EvangelionHUD,
        PlayerInfoFrame = PlayerInfoFrame,
        PlayerImage = PlayerImage,
        PlayerNameText = PlayerNameText,
        HealthBarBackground = HealthBarBackground,
        HealthBarFill = HealthBarFill
    }
end

local uiElements = createEvangelionHUD()
local PlayerImage = uiElements.PlayerImage
local HealthBarFill = uiElements.HealthBarFill

local function onCharacterSpawned(character)
    local humanoid = character:WaitForChild("Humanoid")

    if PlayerImage.Image == "" then
        local success, content = pcall(function()
            return Players:GetUserThumbnailAsync(LocalPlayer.UserId, Enum.ThumbnailType.HeadShot, Enum.ThumbnailSize.Size420x420)
        end)
        if success and content then
            PlayerImage.Image = content
            PlayerImage.BackgroundTransparency = 0
        else
        end
    end

    local function updateHealthBar()
        local currentHealth = humanoid.Health
        local maxHealth = humanoid.MaxHealth
        local healthRatio = currentHealth / maxHealth

        HealthBarFill.Size = UDim2.new(healthRatio, 0, 1, 0)

        if healthRatio > 0.6 then
            HealthBarFill.BackgroundColor3 = Color3.fromRGB(0, 255, 0)
        elseif healthRatio > 0.3 then
            HealthBarFill.BackgroundColor3 = Color3.fromRGB(255, 255, 0)
        else
            HealthBarFill.BackgroundColor3 = Color3.fromRGB(255, 0, 0)
        end
    end

    local healthChangedConnection
    healthChangedConnection = humanoid.HealthChanged:Connect(updateHealthBar)

    character.Destroying:Connect(function()
        if healthChangedConnection then
            healthChangedConnection:Disconnect()
        end
    end)

    updateHealthBar()
end

LocalPlayer.CharacterAdded:Connect(onCharacterSpawned)

if LocalPlayer.Character then
    onCharacterSpawned(LocalPlayer.Character)
end
sound.Volume = 2.5
