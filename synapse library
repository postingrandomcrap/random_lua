local windows =  {}

local UIClosed = -0.4, 0,0.271, 0
local UIOpened = 0.0109783234, 0, 0.191451475, 0

local Opened = true

local TS = game.TweenService

function windows:Create(options)


    local github = options.GitHubLink
    local title = options.Title
    local GameName = options.Game
    game.StarterGui:SetCore("SendNotification", {
        Title = title,
        Text = "Welcome To "..title..""..game.Players.LocalPlayer.DisplayName.." AKA "..game.Players.LocalPlayer.Name.."!",
        Duration = 5,
        Logo = "rbxassetid://7072724538",
    })

    local LunaLibrary = Instance.new("ScreenGui")
    local UIS = game:GetService("UserInputService")

    local backFrame = Instance.new("Frame")

    local ImageLabel = Instance.new("ImageLabel")

    --Properties:
    
    ImageLabel.Parent = backFrame
    ImageLabel.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
    ImageLabel.BackgroundTransparency = 1.000
    ImageLabel.Position = UDim2.new(-0.0542949736, 0, -0.0541900061, 0)
    ImageLabel.Size = UDim2.new(0, 676, 0, 352)
    ImageLabel.Image = "http://www.roblox.com/asset/?id=7429253275"
    ImageLabel.ImageColor3 = Color3.fromRGB(0, 0, 0)

    local UIS = game:GetService('UserInputService')

    local maincorner = Instance.new("UICorner")
    local allPages = Instance.new("Frame")
    local maincorner_2 = Instance.new("UICorner")
    local Pages = Instance.new("Folder")

    local mainCorner = Instance.new("UICorner")
    local maincorner_3 = Instance.new("UICorner")
    local Title = Instance.new("TextLabel")
    local Game = Instance.new("TextLabel")
    local Exit = Instance.new("ImageButton")
    local topBar = Instance.new("Frame")
    local maincorner_4 = Instance.new("UICorner")
    local UIListLayout = Instance.new("UIListLayout")
 

    local Frame = Instance.new("Frame")
    local Minimize = Instance.new("TextButton")
    local newPage = Instance.new("Frame")

    newPage.Name = "newPage"
    newPage.Parent = allPages
    newPage.BackgroundColor3 = Color3.fromRGB(32, 32, 32)
    newPage.ClipsDescendants = true
    newPage.Position = UDim2.new(0.012, 0,0.026, 0)
    newPage.Size = UDim2.new(0, 582, 0, 237)

    --Properties:

    for i,v in pairs(game.CoreGui:GetChildren()) do
        if v.Name == "Luna Library" then
            v:Destroy()
        end
    end

    local UIS = game:GetService('UserInputService')
    local frame = backFrame
    local dragToggle = nil
    local dragSpeed = 0.15
    local dragStart = nil
    local startPos = nil
    
    local function updateInput(input)
        local delta = input.Position - dragStart
        local position = UDim2.new(startPos.X.Scale, startPos.X.Offset + delta.X,
            startPos.Y.Scale, startPos.Y.Offset + delta.Y)
        game:GetService('TweenService'):Create(frame, TweenInfo.new(dragSpeed), {Position = position}):Play()
    end
    
    frame.InputBegan:Connect(function(input)
        if (input.UserInputType == Enum.UserInputType.MouseButton1 or input.UserInputType == Enum.UserInputType.Touch) then 
            dragToggle = true
            dragStart = input.Position
            startPos = frame.Position
            input.Changed:Connect(function()
                if input.UserInputState == Enum.UserInputState.End then
                    dragToggle = false
                end
            end)
        end
    end)
    
    UIS.InputChanged:Connect(function(input)
        if input.UserInputType == Enum.UserInputType.MouseMovement or input.UserInputType == Enum.UserInputType.Touch then
            if dragToggle then
                updateInput(input)
            end
        end
    end)
    

    LunaLibrary.Name = "Luna Library"
    LunaLibrary.Parent = game.CoreGui
    LunaLibrary.ZIndexBehavior = Enum.ZIndexBehavior.Sibling

    backFrame.Name = "backFrame"
    backFrame.Parent = LunaLibrary
    backFrame.BackgroundColor3 = Color3.fromRGB(32, 32, 32)
    backFrame.ClipsDescendants = false
    backFrame.Position = UDim2.new(0.314547002, 0, 0.306092143, 0)
    backFrame.Size = UDim2.new(0, 610, 0, 318)

    maincorner.CornerRadius = UDim.new(0, 6)
    maincorner.Name = "maincorner"
    maincorner.Parent = backFrame

    allPages.Name = "allPages"
    allPages.Parent = backFrame
    allPages.BackgroundColor3 = Color3.fromRGB(40, 40, 40)
    allPages.ClipsDescendants = true
    allPages.Position = UDim2.new(0.0109783234, 0, 0.191451475, 0)
    allPages.Size = UDim2.new(0, 596, 0, 249)

    maincorner_2.CornerRadius = UDim.new(0, 6)
    maincorner_2.Name = "maincorner"
    maincorner_2.Parent = allPages

    Pages.Name = "Pages"
    Pages.Parent = allPages




    maincorner_3.CornerRadius = UDim.new(0, 4)
    maincorner_3.Name = "maincorner"
    maincorner_3.Parent = newPage

    Title.Name = "Title"
    Title.Parent = backFrame
    Title.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
    Title.BackgroundTransparency = 1.000
    Title.Position = UDim2.new(0.010118044, 0, 0, 0)
    Title.Size = UDim2.new(0, 77, 0, 33)
    Title.Font = Enum.Font.GothamBold
    Title.Text = title.." | "
    Title.TextColor3 = Color3.fromRGB(255, 255, 255)
    Title.TextScaled = true
    Title.TextSize = 14.000
    Title.TextWrapped = true
    Title.TextXAlignment = Enum.TextXAlignment.Left

    Game.Name = "game"
    Game.Parent = backFrame
    Game.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
    Game.BackgroundTransparency = 1.000
    Game.Position = UDim2.new(0.146183595, 0, 0, 0)
    Game.Size = UDim2.new(0, 179, 0, 33)
    Game.Font = Enum.Font.GothamBold
    Game.Text = GameName
    Game.TextColor3 = Color3.fromRGB(255, 255, 255)
    Game.TextSize = 14.000
    Game.TextStrokeTransparency = 0.900
    Game.TextTransparency = 0.770
    Game.TextWrapped = true
    Game.TextXAlignment = Enum.TextXAlignment.Left

    Exit.Name = "Exit"
    Exit.Parent = backFrame
    Exit.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
    Exit.BackgroundTransparency = 1.000
    Exit.Position = UDim2.new(0.952782452, 0, 0.0178571437, 0)
    Exit.Size = UDim2.new(0, 21, 0, 21)
    Exit.Image = "rbxassetid://7072725342"
    Exit.MouseEnter:Connect(function()
        TS:Create(Exit, TweenInfo.new(0.2, Enum.EasingStyle.Linear, Enum.EasingDirection.In), {
            ImageColor3 = Color3.fromRGB(255, 77, 77)
        }):Play()
    end)

    Exit.MouseLeave:Connect(function()
        TS:Create(Exit, TweenInfo.new(0.2, Enum.EasingStyle.Linear, Enum.EasingDirection.In), {
            ImageColor3 = Color3.fromRGB(255, 255, 255)
        }):Play()
    end)

    Exit.MouseButton1Click:Connect(function()
        TS:Create(backFrame, TweenInfo.new(0.4, Enum.EasingStyle.Circular, Enum.EasingDirection.In), {
            Position = UDim2.new(-0.4, 0,0.271, 0)
        }):Play()
        wait(1)
        game.CoreGui["Luna Library"]:Destroy()
    end)

    topBar.Name = "topBar"
    topBar.Parent = backFrame
    topBar.BackgroundColor3 = Color3.fromRGB(32, 32, 32)
    topBar.BackgroundTransparency = 1.000
    topBar.ClipsDescendants = true
    topBar.Position = UDim2.new(0.0109783234, 0, 0.0982142836, 0)
    topBar.Size = UDim2.new(0, 626, 0, 33)

    maincorner_4.CornerRadius = UDim.new(0, 6)
    maincorner_4.Name = "maincorner"
    maincorner_4.Parent = topBar

    UIListLayout.Parent = topBar
    UIListLayout.FillDirection = Enum.FillDirection.Horizontal
    UIListLayout.SortOrder = Enum.SortOrder.LayoutOrder





    Frame.Parent = backFrame
    Frame.BackgroundColor3 = Color3.fromRGB(45, 45, 45)
    Frame.BorderColor3 = Color3.fromRGB(45, 45, 45)
    Frame.BorderSizePixel = 0
    Frame.Position = UDim2.new(0, 0, 0.0900000036, 0)
    Frame.Size = UDim2.new(0, 610, 0, 1)

    Minimize.Name = "Minimize"
    Minimize.Parent = backFrame
    Minimize.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
    Minimize.BackgroundTransparency = 1.000
    Minimize.Position = UDim2.new(0.908196747, 0, 0.0178571008, 0)
    Minimize.Size = UDim2.new(0, 27, 0, 27)
    Minimize.Font = Enum.Font.GothamBold
    Minimize.Text = "-"
    Minimize.TextColor3 = Color3.fromRGB(255, 255, 255)
    Minimize.TextSize = 14.000
    Minimize.MouseEnter:Connect(function()
        TS:Create(Minimize, TweenInfo.new(0.145, Enum.EasingStyle.Quad, Enum.EasingDirection.In), {
            TextColor3 = Color3.fromRGB(255, 166, 0)
        }):Play()
    end)
    Minimize.MouseLeave:Connect(function()
        TS:Create(Minimize, TweenInfo.new(0.145, Enum.EasingStyle.Quad, Enum.EasingDirection.In), {
            TextColor3 = Color3.fromRGB(255, 255, 255)
        }):Play()
    end)

    local Closed = false

    Minimize.MouseButton1Click:Connect(function()
        Closed = true
        TS:Create(backFrame, TweenInfo.new(0.3, Enum.EasingStyle.Quad, Enum.EasingDirection.In), {
            Position = UDim2.new(UIClosed)
        }):Play()
        game.StarterGui:SetCore("SendNotification", {
            Title = title,
            Text = "UI Has Been Closed, Press Left Alt On Your Keyboard To ReOpen The GUI."
        })
    end)

    local UIS = game:GetService("UserInputService")

    UIS.InputBegan:Connect(function(KeyCode)
        if KeyCode.KeyCode == Enum.KeyCode.LeftAlt then
            if Closed then
                Closed = false
                TS:Create(backFrame, TweenInfo.new(0.3, Enum.EasingStyle.Linear, Enum.EasingDirection.In), {
                    Position = UDim2.new(0.315, 0,0.306, 0)
                }):Play()
            end
        end
    end)

    --[[local BackgroundTransparency = Instance.new("Frame")
    local transparentCorner = Instance.new("UICorner")
    local Settings = Instance.new("Frame")
    local MainCorner = Instance.new("UICorner")
    local Exit = Instance.new("ImageButton")
    local PageLogo = Instance.new("ImageLabel")
    local TextLabel = Instance.new("TextLabel")
    local Settings_2 = Instance.new("ImageButton")
    local Check = Instance.new("Frame")
    
    --Properties:
    
    BackgroundTransparency.Name = "BackgroundTransparency"
    BackgroundTransparency.Parent = backFrame
    BackgroundTransparency.BackgroundColor3 = Color3.fromRGB(0, 0, 0)
    BackgroundTransparency.BackgroundTransparency = 1
    BackgroundTransparency.Size = UDim2.new(0, 610, 0, 318)
    
    transparentCorner.CornerRadius = UDim.new(0, 6)
    transparentCorner.Name = "transparentCorner"
    transparentCorner.Parent = BackgroundTransparency
    
    Settings.Name = "Settings"
    Settings.Parent = BackgroundTransparency
    Settings.BackgroundTransparency = 1
    Settings.BackgroundColor3 = Color3.fromRGB(31, 31, 31)
    Settings.Position = UDim2.new(0.050, 0,0.096, 0)
    Settings.Size = UDim2.new(0, 556,0, 267)
    
    MainCorner.CornerRadius = UDim.new(0, 6)
    MainCorner.Name = "MainCorner"
    MainCorner.Parent = Settings
    
    Exit.Name = "Exit"
    Exit.Parent = Settings
    Exit.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
    Exit.BackgroundTransparency = 1.000
    Exit.ImageTransparency = 1
    Exit.Position = UDim2.new(0.952782452, 0, 0.0178571437, 0)
    Exit.Size = UDim2.new(0, 21, 0, 21)
    Exit.Image = "rbxassetid://7072725342"
    
    PageLogo.Name = "PageLogo"
    PageLogo.Parent = Settings
    PageLogo.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
    PageLogo.BackgroundTransparency = 1.000
    PageLogo.ImageTransparency = 1
    PageLogo.Position = UDim2.new(0.00999999978, 0, 0.0149999997, 0)
    PageLogo.Size = UDim2.new(0, 20, 0, 20)
    PageLogo.Image = "rbxassetid://7072721682"
    
    TextLabel.Parent = Settings
    TextLabel.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
    TextLabel.BackgroundTransparency = 1.000
    TextLabel.Position = UDim2.new(0.440647483, 0, 0.0299625471, 0)
    TextLabel.Size = UDim2.new(0, 54, 0, 17)
    TextLabel.Font = Enum.Font.Gotham
    TextLabel.Text = "Settings"
    TextLabel.TextColor3 = Color3.fromRGB(255, 255, 255)
    TextLabel.TextSize = 14.000
    TextLabel.TextTransparency = 1
    TextLabel.TextXAlignment = Enum.TextXAlignment.Left
    

    local SettingsListing = Instance.new("Frame")
    local SettingsCorner = Instance.new("UICorner")
    local SettingsLayout = Instance.new("UIListLayout")

    --Properties:

    SettingsListing.Name = "SettingsListing"
    SettingsListing.Parent = Settings
    SettingsListing.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
    SettingsListing.BackgroundTransparency = 1
    SettingsListing.Position = UDim2.new(0.01, 0,0.115, 0)
    SettingsListing.Size = UDim2.new(0, 545,0, 228)

    SettingsCorner.CornerRadius = UDim.new(0, 6)
    SettingsCorner.Name = "SettingsCorner"
    SettingsCorner.Parent = SettingsListing

    SettingsLayout.Name = "SettingsLayout"
    SettingsLayout.Parent = SettingsListing
    SettingsLayout.SortOrder = Enum.SortOrder.LayoutOrder

    Settings_2.Name = "Settings"
    Settings_2.Parent = backFrame
    Settings_2.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
    Settings_2.BackgroundTransparency = 1.000
    Settings_2.Position = UDim2.new(0.483606517, 0, 0.0178571008, 0)
    Settings_2.Size = UDim2.new(0, 17, 0, 17)
    Settings_2.Image = "rbxassetid://7072721682"
    Settings_2.ImageTransparency = 0.630

    local Error = Instance.new("TextButton")
    local Butoncorner = Instance.new("UICorner")

    --Properties:

    Error.Name = "Error"
    Error.Parent = SettingsListing
    Error.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
    Error.BackgroundTransparency = 1.000
    Error.Size = UDim2.new(0, 542, 0, 229)
    Error.Font = Enum.Font.SourceSansSemibold
    Error.Text = "Settings Are Currently Being Worked On Right Now, Come Back Later."
    Error.TextColor3 = Color3.fromRGB(255, 255, 255)
    Error.TextTransparency = 1
    Error.TextScaled = true
    Error.TextSize = 42.000
    Error.Visible = false
    Error.TextWrapped = true

    Butoncorner.CornerRadius = UDim.new(0, 6)
    Butoncorner.Name = "Butoncorner"
    Butoncorner.Parent = Error
    Settings_2.MouseEnter:Connect(function()
        TS:Create(Settings_2, TweenInfo.new(0.2, Enum.EasingStyle.Linear, Enum.EasingDirection.In), {
            ImageTransparency = 0
        }):Play()   
    end)
    Settings_2.MouseLeave:Connect(function()
        TS:Create(Settings_2, TweenInfo.new(0.2, Enum.EasingStyle.Linear, Enum.EasingDirection.In), {
            ImageTransparency = 0.630
        }):Play()   
    end)

    Settings_2.MouseButton1Click:Connect(function()
        Error.Visible = true
        TS:Create(BackgroundTransparency, TweenInfo.new(0.2, Enum.EasingStyle.Linear, Enum.EasingDirection.In), {
            BackgroundTransparency = 0.550
        }):Play()  
        TS:Create(Error, TweenInfo.new(0.2, Enum.EasingStyle.Linear, Enum.EasingDirection.In), {
            TextTransparency = 0
        }):Play()
        TS:Create(Settings, TweenInfo.new(0.2, Enum.EasingStyle.Linear, Enum.EasingDirection.In), {
            BackgroundTransparency = 0
        }):Play()  
        TS:Create(SettingsListing, TweenInfo.new(0.2, Enum.EasingStyle.Linear, Enum.EasingDirection.In), {
            BackgroundTransparency = 1
        }):Play()  
        TS:Create(Exit, TweenInfo.new(0.2, Enum.EasingStyle.Linear, Enum.EasingDirection.In), {
            ImageTransparency = 0
        }):Play()   
        TS:Create(PageLogo, TweenInfo.new(0.2, Enum.EasingStyle.Linear, Enum.EasingDirection.In), {
            ImageTransparency = 0.3
        }):Play()  
        TS:Create(TextLabel, TweenInfo.new(0.2, Enum.EasingStyle.Linear, Enum.EasingDirection.In), {
            TextTransparency = 0.520
        }):Play() 
    end)

    Exit.MouseEnter:Connect(function()
        TS:Create(Exit, TweenInfo.new(0.2, Enum.EasingStyle.Linear, Enum.EasingDirection.In), {
            ImageColor3 = Color3.fromRGB(255, 77, 77)
        }):Play()
    end)

    Exit.MouseLeave:Connect(function()
        TS:Create(Exit, TweenInfo.new(0.2, Enum.EasingStyle.Linear, Enum.EasingDirection.In), {
            ImageColor3 = Color3.fromRGB(255, 255, 255)
        }):Play()
    end)

    Exit.MouseButton1Click:Connect(function()
        Error.Visible = false
        TS:Create(BackgroundTransparency, TweenInfo.new(0.2, Enum.EasingStyle.Linear, Enum.EasingDirection.In), {
            BackgroundTransparency = 1
        }):Play()   
        TS:Create(Error, TweenInfo.new(0.2, Enum.EasingStyle.Linear, Enum.EasingDirection.In), {
            TextTransparency = 1
        }):Play()
        TS:Create(Settings, TweenInfo.new(0.2, Enum.EasingStyle.Linear, Enum.EasingDirection.In), {
            --Position = UDim2.new(0.955, 0,1.323, 0)
            BackgroundTransparency = 1
        }):Play()  
        TS:Create(Exit, TweenInfo.new(0.2, Enum.EasingStyle.Linear, Enum.EasingDirection.In), {
            --Position = UDim2.new(0.955, 0,1.323, 0)
            ImageTransparency = 1
        }):Play()   
        TS:Create(PageLogo, TweenInfo.new(0.2, Enum.EasingStyle.Linear, Enum.EasingDirection.In), {
            --Position = UDim2.new(0.955, 0,1.323, 0)
            ImageTransparency = 1
        }):Play()  
        TS:Create(TextLabel, TweenInfo.new(0.2, Enum.EasingStyle.Linear, Enum.EasingDirection.In), {
            --Position = UDim2.new(0.955, 0,1.323, 0)
            TextTransparency = 1
        }):Play() 
    end)]]--

    local tabs = {}

    function tabs:NewTab(options)
        local ImageLabel = Instance.new("ImageLabel")

        local title = options.Title
        local page = Instance.new("ScrollingFrame")
        local elementsListing = Instance.new("UIListLayout")
        local tabButton = Instance.new("TextButton")
        local tabButtonCorner = Instance.new("UICorner")
        local Logo = Instance.new("ImageLabel")
        local Title_2 = Instance.new("TextLabel")


        ImageLabel.Parent = topBar
        ImageLabel.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
        ImageLabel.BackgroundTransparency = 1.000
        ImageLabel.Size = UDim2.new(0, 120, 0, 33)
        ImageLabel.Image = "http://www.roblox.com/asset/?id=9313786480"
        ImageLabel.ScaleType = Enum.ScaleType.Tile

        tabButton.Name = "tabButton"
        tabButton.Parent = ImageLabel
        tabButton.BackgroundColor3 = Color3.fromRGB(45, 45, 45)
        tabButton.Position = UDim2.new(-0.000598669052, 0, -0.00182622671, 0)
        tabButton.Size = UDim2.new(0, 117, 0, 26)
        tabButton.AutoButtonColor = false
        tabButton.Font = Enum.Font.GothamSemibold
        tabButton.Text = ""
        tabButton.TextColor3 = Color3.fromRGB(255, 255, 255)
        tabButton.TextSize = 14.000
    
        tabButtonCorner.CornerRadius = UDim.new(0, 5)
        tabButtonCorner.Name = "tabButtonCorner"
        tabButtonCorner.Parent = tabButton
    
        Logo.Name = "Logo"
        Logo.Parent = tabButton
        Logo.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
        Logo.BackgroundTransparency = 1.000
        Logo.Position = UDim2.new(0.0627408773, 0, 0.203377947, 0)
        Logo.Size = UDim2.new(0, 15, 0, 14)
        Logo.ImageTransparency = 0.63
        Logo.Image = "rbxassetid://7072724538"
    
        Title_2.Name = "Title"
        Title_2.Parent = tabButton
        Title_2.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
        Title_2.BackgroundTransparency = 1.000
        Title_2.Position = UDim2.new(0.240487903, 0, 0.169481725, 0)
        Title_2.Size = UDim2.new(0, 89, 0, 17)
        Title_2.Font = Enum.Font.GothamBold
        Title_2.Text = title
        Title_2.TextTransparency = 0.63
        Title_2.TextColor3 = Color3.fromRGB(255, 255, 255)
        Title_2.TextSize = 11.000
        Title_2.TextXAlignment = Enum.TextXAlignment.Left

        page.Name = "page"
        page.Parent = Pages
        page.Active = true
        page.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
        page.BackgroundTransparency = 1.000
        page.BorderSizePixel = 0
        page.Position = UDim2.new(0.026, 0,0.052, 0)
        page.Size = UDim2.new(0, 567, 0, 223)
        page.ScrollBarThickness = 0
        page.Visible = false
    
        elementsListing.Name = "elementsListing"
        elementsListing.Parent = page
        elementsListing.SortOrder = Enum.SortOrder.LayoutOrder
        elementsListing.Padding = UDim.new(0, 7)
    
        mainCorner.CornerRadius = UDim.new(0, 4)
        mainCorner.Name = "mainCorner"
        mainCorner.Parent = page
        
        elementsListing:GetPropertyChangedSignal("AbsoluteContentSize"):Connect(function()
            page.CanvasSize = UDim2.new(0,0,0,elementsListing.AbsoluteContentSize.Y) 
        end)

        tabButton.MouseButton1Click:Connect(function()
            for i,v in next, Pages:GetChildren() do
                v.Visible = false
            end
            page.Visible = true

            
            for i,v in next, topBar:GetDescendants() do
                if v.Name == "Title" then 
                    TS:Create(v, TweenInfo.new(0.2, Enum.EasingStyle.Linear, Enum.EasingDirection.In), {
                        TextTransparency = 0.63
                    }):Play()
                end
                if v.Name == "Logo" then 
                    TS:Create(v, TweenInfo.new(0.2, Enum.EasingStyle.Linear, Enum.EasingDirection.In), {
                        ImageTransparency = 0.63
                    }):Play()
                end
            end

            TS:Create(Title_2, TweenInfo.new(0.2, Enum.EasingStyle.Linear, Enum.EasingDirection.In), {
                TextTransparency = 0
            }):Play()
            TS:Create(Logo, TweenInfo.new(0.2, Enum.EasingStyle.Linear, Enum.EasingDirection.In), {
                ImageTransparency = 0
            }):Play()
        end)

        local elements = {}

        function elements:Notification(NotiInfo)
            local Notificationtransparency = Instance.new("Frame")
            local NotificationtransparencyCorner = Instance.new("UICorner")
            local NotificationMenuBackground = Instance.new("Frame")
            local NotificationMenuCorner = Instance.new("UICorner")
            local TopBarCover = Instance.new("Frame")
            local BarCoverCorner = Instance.new("UICorner")
            local ExitNoti = Instance.new("ImageButton")
            local Icon = Instance.new("ImageLabel")
            local TextLabel = Instance.new("TextLabel")
            local NotificationMenu = Instance.new("Frame")
            local MenuCorner = Instance.new("UICorner")
            local NotiInfo = Instance.new("TextLabel")

            --Properties:

            Notificationtransparency.Name = "Notificationtransparency"
            Notificationtransparency.Parent = backFrame
            Notificationtransparency.BackgroundColor3 = Color3.fromRGB(0, 0, 0)
            Notificationtransparency.BackgroundTransparency = 0.550
            Notificationtransparency.BorderSizePixel = 0
            Notificationtransparency.Position = UDim2.new(0.00163934426, 0, 0, 0)
            Notificationtransparency.Size = UDim2.new(0, 609, 0, 318)

            NotificationtransparencyCorner.CornerRadius = UDim.new(0, 6)
            NotificationtransparencyCorner.Name = "NotificationtransparencyCorner"
            NotificationtransparencyCorner.Parent = Notificationtransparency

            NotificationMenuBackground.Name = "NotificationMenuBackground"
            NotificationMenuBackground.Parent = Notificationtransparency
            NotificationMenuBackground.BackgroundColor3 = Color3.fromRGB(34, 34, 34)
            NotificationMenuBackground.BorderSizePixel = 0
            NotificationMenuBackground.Position = UDim2.new(0.0853503644, 0, 0.1223443, 0)
            NotificationMenuBackground.Size = UDim2.new(0, 506, 0, 240)

            NotificationMenuCorner.CornerRadius = UDim.new(0, 6)
            NotificationMenuCorner.Name = "NotificationMenuCorner"
            NotificationMenuCorner.Parent = NotificationMenuBackground

            TopBarCover.Name = "TopBarCover"
            TopBarCover.Parent = NotificationMenuBackground
            TopBarCover.BackgroundColor3 = Color3.fromRGB(58, 58, 58)
            TopBarCover.BorderSizePixel = 0
            TopBarCover.Position = UDim2.new(0, 0, 0.109922916, 0)
            TopBarCover.Size = UDim2.new(0, 505, 0, 1)

            BarCoverCorner.CornerRadius = UDim.new(0, 6)
            BarCoverCorner.Name = "BarCoverCorner"
            BarCoverCorner.Parent = TopBarCover

            ExitNoti.Name = "ExitNoti"
            ExitNoti.Parent = TopBarCover
            ExitNoti.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
            ExitNoti.BackgroundTransparency = 1.000
            ExitNoti.Position = UDim2.new(0.952782452, 0, -24.9821434, 0)
            ExitNoti.Size = UDim2.new(0, 21, 0, 21)
            ExitNoti.Image = "rbxassetid://7072725342"

            Icon.Name = "Icon"
            Icon.Parent = NotificationMenuBackground
            Icon.BackgroundTransparency = 1.000
            Icon.Position = UDim2.new(0.00790513679, 0, 0.0166666675, 0)
            Icon.Size = UDim2.new(0.0357871093, 0, 0.0765895844, 0)
            Icon.Image = "rbxassetid://7072720243"

            TextLabel.Parent = NotificationMenuBackground
            TextLabel.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
            TextLabel.BackgroundTransparency = 1.000
            TextLabel.Size = UDim2.new(0, 505, 0, 26)
            TextLabel.Font = Enum.Font.Gotham
            TextLabel.Text = "Notification"
            TextLabel.TextColor3 = Color3.fromRGB(255, 255, 255)
            TextLabel.TextSize = 14.000

            NotificationMenu.Name = "NotificationMenu"
            NotificationMenu.Parent = NotificationMenuBackground
            NotificationMenu.BackgroundColor3 = Color3.fromRGB(30, 30, 30)
            NotificationMenu.BorderSizePixel = 0
            NotificationMenu.Position = UDim2.new(0.0102514941, 0, 0.13067767, 0)
            NotificationMenu.Size = UDim2.new(0, 493, 0, 202)

            MenuCorner.CornerRadius = UDim.new(0, 6)
            MenuCorner.Name = "MenuCorner"
            MenuCorner.Parent = NotificationMenu

            NotiInfo.Name = "NotiInfo"
            NotiInfo.Parent = NotificationMenuBackground
            NotiInfo.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
            NotiInfo.BackgroundTransparency = 1.000
            NotiInfo.Position = UDim2.new(0.0436922461, 0, 0.188841119, 0)
            NotiInfo.Size = UDim2.new(0, 460, 0, 170)
            NotiInfo.Font = Enum.Font.Gotham
            NotiInfo.Text = "Button Pressed!"
            NotiInfo.TextColor3 = Color3.fromRGB(255, 255, 255)
            NotiInfo.TextSize = 19.000
        end

        function elements:Button(options)
            local title = options.Title or "Button Example"
            local Callback = options.Callback or function() end

            local TextButton = Instance.new("TextButton")
            local ButtonCorner = Instance.new("UICorner")

            --Properties:

            TextButton.Parent = page
            TextButton.BackgroundColor3 = Color3.fromRGB(45, 45, 45)
            TextButton.BorderSizePixel = 0
            TextButton.Position = UDim2.new(0.0405643731, 0, -0.185653999, 0)
            TextButton.Size = UDim2.new(0, 567, 0, 31)
            TextButton.Font = Enum.Font.GothamBold
            TextButton.Text = title
            TextButton.TextColor3 = Color3.fromRGB(255, 255, 255)
            TextButton.TextSize = 14.000
            TextButton.AutoButtonColor = false

            ButtonCorner.CornerRadius = UDim.new(0, 4)
            ButtonCorner.Name = "ButtonCorner"
            ButtonCorner.Parent = TextButton
            TextButton.MouseButton1Click:Connect(function()
                TS:Create(TextButton, TweenInfo.new(0.08, Enum.EasingStyle.Linear, Enum.EasingDirection.In), {
                    BackgroundColor3 = Color3.fromRGB(180,180,180)
                }):Play()  
                wait(0.08)
                TS:Create(TextButton, TweenInfo.new(0.08, Enum.EasingStyle.Linear, Enum.EasingDirection.In), {
                    BackgroundColor3 = Color3.fromRGB(39,39,39)
                }):Play()  
                Callback()
            end)
            TextButton.MouseEnter:Connect(function()
                TS:Create(TextButton, TweenInfo.new(0.2, Enum.EasingStyle.Linear, Enum.EasingDirection.In), {
                    BackgroundColor3 = Color3.fromRGB(61, 61, 61)
                }):Play()
            end)
            TextButton.MouseLeave:Connect(function()
                TS:Create(TextButton, TweenInfo.new(0.2, Enum.EasingStyle.Linear, Enum.EasingDirection.In), {
                    BackgroundColor3 = Color3.fromRGB(45, 45, 45)
                }):Play()
            end)
        end

        function elements:Toggle(options)
            local title = options.Title or "Toggle Info"
            local desc = options.Description or "Toggle Description Here."
            local Callback = options.Callback or function() end

            local Toggle = Instance.new("TextButton")
            local Description = Instance.new("TextLabel")
            local Title = Instance.new("TextLabel")
            local Outer = Instance.new("Frame")
            local Inner = Instance.new("Frame")
            local Check = Instance.new("ImageLabel")
            local InnerCorner = Instance.new("UICorner")
            local OuterCorner = Instance.new("UICorner")
            local ToggleCorner = Instance.new("UICorner")

            --Properties:

            Toggle.Name = "Toggle"
            Toggle.Parent = page
            Toggle.BackgroundColor3 = Color3.fromRGB(32, 32, 32)
            Toggle.BorderSizePixel = 0
            Toggle.Position = UDim2.new(0, 0, 0.156950817, 0)
            Toggle.Size = UDim2.new(0, 567, 0, 35)
            Toggle.AutoButtonColor = false
            Toggle.Font = Enum.Font.GothamBold
            Toggle.Text = ""
            Toggle.TextColor3 = Color3.fromRGB(255, 255, 255)
            Toggle.TextSize = 14.000

            Description.Name = "Description"
            Description.Parent = Toggle
            Description.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
            Description.BackgroundTransparency = 1.000
            Description.Position = UDim2.new(0.0723104104, 0, 0.574026048, 0)
            Description.Size = UDim2.new(0, 520, 0, 12)
            Description.Font = Enum.Font.Gotham
            Description.Text = desc
            Description.TextColor3 = Color3.fromRGB(255, 255, 255)
            Description.TextSize = 13.000
            Description.TextTransparency = 0.750
            Description.TextXAlignment = Enum.TextXAlignment.Left

            Title.Name = "Title"
            Title.Parent = Toggle
            Title.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
            Title.BackgroundTransparency = 1.000
            Title.Position = UDim2.new(0.072310403, 0, 0.0303030312, 0)
            Title.Size = UDim2.new(0, 200, 0, 20)
            Title.Font = Enum.Font.Gotham
            Title.Text = title
            Title.TextColor3 = Color3.fromRGB(255, 255, 255)
            Title.TextSize = 16.000
            Title.TextXAlignment = Enum.TextXAlignment.Left

            Outer.Name = "Outer"
            Outer.Parent = Toggle
            Outer.BackgroundColor3 = Color3.fromRGB(45, 45, 45)
            Outer.Size = UDim2.new(0, 32, 0, 33)

            Inner.Name = "Inner"
            Inner.Parent = Outer
            Inner.BackgroundColor3 = Color3.fromRGB(32, 32, 32)
            Inner.Position = UDim2.new(0.0590000004, 0, 0.0500000007, 0)
            Inner.Selectable = true
            Inner.Size = UDim2.new(0, 28, 0, 29)

            Check.Name = "Check"
            Check.Parent = Inner
            Check.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
            Check.BackgroundTransparency = 1.000
            Check.Position = UDim2.new(0.0357142799, 0, 0.103448279, 0)
            Check.Size = UDim2.new(0, 25, 0, 25)
            Check.ImageTransparency = 1
            Check.Image = "rbxassetid://7072706620"

            InnerCorner.CornerRadius = UDim.new(0, 2)
            InnerCorner.Name = "InnerCorner"
            InnerCorner.Parent = Inner

            OuterCorner.CornerRadius = UDim.new(0, 3)
            OuterCorner.Name = "OuterCorner"
            OuterCorner.Parent = Outer

            ToggleCorner.CornerRadius = UDim.new(0, 4)
            ToggleCorner.Name = "ToggleCorner"
            ToggleCorner.Parent = Toggle
            
            local toggled = false

            Toggle.MouseButton1Click:Connect(function()
                toggled = not toggled
                Callback(toggled)

                if toggled then
                    TS:Create(Inner, TweenInfo.new(0.15, Enum.EasingStyle.Linear, Enum.EasingDirection.In), {
                        BackgroundColor3 = Color3.fromRGB(123, 190, 239)
                    }):Play()
                    TS:Create(Check, TweenInfo.new(0.15, Enum.EasingStyle.Linear, Enum.EasingDirection.In), {
                        ImageTransparency = 0
                    }):Play()
                else
                    TS:Create(Inner, TweenInfo.new(0.15, Enum.EasingStyle.Linear, Enum.EasingDirection.In), {
                        BackgroundColor3 = Color3.fromRGB(32, 32, 32)
                    }):Play()
                    TS:Create(Check, TweenInfo.new(0.15, Enum.EasingStyle.Linear, Enum.EasingDirection.In), {
                        ImageTransparency = 1
                    }):Play()
                end
            end)
        end

        function elements:Label(options)
            local title = options.Title or "This Is A Label."

            local Label = Instance.new("TextLabel")
            local Inner = Instance.new("TextLabel")
            local LabelCorner = Instance.new("UICorner")
            local LabelCorner_2 = Instance.new("UICorner")
            
            --Properties:
            
            Label.Name = "Label"
            Label.Parent = page
            Label.BackgroundColor3 = Color3.fromRGB(35, 35, 35)
            Label.Position = UDim2.new(0.00153139362, 0, 0.00420171767, 0)
            Label.Size = UDim2.new(0, 567, 0, 27)
            Label.Font = Enum.Font.GothamBold
            Label.Text = ""
            Label.TextColor3 = Color3.fromRGB(255, 255, 255)
            Label.TextSize = 15.000
            
            Inner.Name = "Inner"
            Inner.Parent = Label
            Inner.BackgroundColor3 = Color3.fromRGB(45, 45, 45)
            Inner.Position = UDim2.new(0.00352733675, 0, 0.111111112, 0)
            Inner.Size = UDim2.new(0, 562, 0, 21)
            Inner.Font = Enum.Font.GothamBold
            Inner.Text = title
            Inner.TextColor3 = Color3.fromRGB(255, 255, 255)
            Inner.TextSize = 15.000
            
            LabelCorner.CornerRadius = UDim.new(0, 4)
            LabelCorner.Name = "LabelCorner"
            LabelCorner.Parent = Inner
            
            LabelCorner_2.CornerRadius = UDim.new(0, 4)
            LabelCorner_2.Name = "LabelCorner"
            LabelCorner_2.Parent = Label
        end

        function elements:TextBox(options)
            local title = options.Title or "textbox"
            local placeholder = options.PlaceHolder or "PlaceHolder here..."
            local Callback = options.Callback or function() end
            local TextBox = Instance.new("Frame")
            local TextBoxTitle = Instance.new("TextLabel")
            local TextBoxOuter = Instance.new("Frame")
            local ActuallTextBox = Instance.new("TextBox")
            local TextBoxCorner = Instance.new("UICorner")
            local OuterCornertextbox = Instance.new("UICorner")
            
            --Properties:
            
            TextBox.Name = "TextBox"
            TextBox.Parent = page
            TextBox.BackgroundColor3 = Color3.fromRGB(32, 32, 32)
            TextBox.BorderSizePixel = 0
            TextBox.Position = UDim2.new(0, 0, 0.215246633, 0)
            TextBox.Size = UDim2.new(0, 567, 0, 63)
            
            TextBoxTitle.Name = "TextBoxTitle"
            TextBoxTitle.Parent = TextBox
            TextBoxTitle.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
            TextBoxTitle.BackgroundTransparency = 1.000
            TextBoxTitle.Position = UDim2.new(0.0123456791, 0, 0, 0)
            TextBoxTitle.Size = UDim2.new(0, 200, 0, 16)
            TextBoxTitle.Font = Enum.Font.Gotham
            TextBoxTitle.Text = title
            TextBoxTitle.TextColor3 = Color3.fromRGB(255, 255, 255)
            TextBoxTitle.TextSize = 13.000
            TextBoxTitle.TextXAlignment = Enum.TextXAlignment.Left
            
            TextBoxOuter.Name = "TextBoxOuter"
            TextBoxOuter.Parent = TextBox
            TextBoxOuter.BackgroundColor3 = Color3.fromRGB(26, 26, 26)
            TextBoxOuter.Position = UDim2.new(0.009, 0,0.473, 0)
            TextBoxOuter.Size = UDim2.new(0, 557, 0, 24)
            
            ActuallTextBox.Name = "ActuallTextBox"
            ActuallTextBox.Parent = TextBoxOuter
            ActuallTextBox.BackgroundColor3 = Color3.fromRGB(45, 45, 45)
            ActuallTextBox.Position = UDim2.new(-0.00200002454, 0, -0.25, 0)
            ActuallTextBox.Size = UDim2.new(0, 558, 0, 27)
            ActuallTextBox.Font = Enum.Font.Gotham
            ActuallTextBox.PlaceholderColor3 = Color3.fromRGB(97, 97, 97)
            ActuallTextBox.PlaceholderText = placeholder
            ActuallTextBox.Text = ""
            ActuallTextBox.TextColor3 = Color3.fromRGB(255, 255, 255)
            ActuallTextBox.TextSize = 14.000
            
            TextBoxCorner.CornerRadius = UDim.new(0, 4)
            TextBoxCorner.Name = "TextBoxCorner"
            TextBoxCorner.Parent = ActuallTextBox
            
            OuterCornertextbox.CornerRadius = UDim.new(0, 4)
            OuterCornertextbox.Name = "OuterCornertextbox"
            OuterCornertextbox.Parent = TextBoxOuter

            ActuallTextBox.Focused:Connect(function()
                game.TweenService:Create(ActuallTextBox, TweenInfo.new(0.15, Enum.EasingStyle.Linear, Enum.EasingDirection.In), {
                    Size = UDim2.new(0, 557,0, 31)
                }):Play()
                game.TweenService:Create(ActuallTextBox, TweenInfo.new(0.15, Enum.EasingStyle.Linear, Enum.EasingDirection.In), {
                    TextColor3 = Color3.fromRGB(255,255,255)
                }):Play()
            end)

            ActuallTextBox.FocusLost:Connect(function()
                Callback(ActuallTextBox.Text)
                game.TweenService:Create(ActuallTextBox, TweenInfo.new(0.15, Enum.EasingStyle.Linear, Enum.EasingDirection.In), {
                    Size = UDim2.new(0, 557, 0, 24)
                }):Play()
                    game.TweenService:Create(ActuallTextBox, TweenInfo.new(0.15, Enum.EasingStyle.Linear, Enum.EasingDirection.In), {
                        TextColor3 = Color3.fromRGB(97, 97, 97)
                    }):Play()

            end)
        end

        function elements:Slider(options)
            local title = options.Title or "Slider Info"
            local minvalue = options.MinValue or 0
            local def = options.Def
            local maxvalue = options.MaxValue or 100
            local callback = options.callback or function() end

            local Slider = Instance.new("Frame")
            local Title = Instance.new("TextLabel")
            local Outer = Instance.new("TextButton")
            local SliderCorner = Instance.new("UICorner")
            local Inner = Instance.new("Frame")
            local SliderInnerCorner = Instance.new("UICorner")
            local Circle = Instance.new("Frame")
            local CircleCorner = Instance.new("UICorner")
            local Title_2 = Instance.new("TextLabel")

            --Properties:

            Slider.Name = "Slider"
            Slider.Parent = page
            Slider.BackgroundColor3 = Color3.fromRGB(32, 32, 32)
            Slider.BorderSizePixel = 0
            Slider.Position = UDim2.new(-0.0158730168, 0, 0.674755335, 0)
            Slider.Size = UDim2.new(0, 567, 0, 41)

            Title.Name = "Title"
            Title.Parent = Slider
            Title.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
            Title.BackgroundTransparency = 1.000
            Title.Position = UDim2.new(0.0123456791, 0, 0, 0)
            Title.Size = UDim2.new(0, 200, 0, 16)
            Title.Font = Enum.Font.GothamSemibold
            Title.Text = title
            Title.TextColor3 = Color3.fromRGB(255, 255, 255)
            Title.TextSize = 14.000
            Title.TextXAlignment = Enum.TextXAlignment.Left

            Outer.Name = "Outer"
            Outer.Parent = Slider
            Outer.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
            Outer.BackgroundTransparency = 0.200
            Outer.Position = UDim2.new(0.00881834235, 0, 0.593170881, 0)
            Outer.Size = UDim2.new(0, 559, 0, 7)
            Outer.AutoButtonColor = false
            Outer.Font = Enum.Font.SourceSans
            Outer.Text = ""
            Outer.TextColor3 = Color3.fromRGB(0, 0, 0)
            Outer.TextSize = 14.000

            SliderCorner.CornerRadius = UDim.new(3434, 8)
            SliderCorner.Name = "SliderCorner"
            SliderCorner.Parent = Outer

            Inner.Name = "Inner"
            Inner.Parent = Outer
            Inner.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
            Inner.BorderSizePixel = 0
            Inner.Size = UDim2.new(0, 0, 0, 7)

            SliderInnerCorner.CornerRadius = UDim.new(3434, 8)
            SliderInnerCorner.Name = "SliderInnerCorner"
            SliderInnerCorner.Parent = Inner

            Circle.Name = "Circle"
            Circle.Parent = Inner
            Circle.BackgroundColor3 = Color3.fromRGB(158, 158, 158)
            Circle.Position = UDim2.new(0.975, 0,-0.571, 0)
            Circle.Size = UDim2.new(0, 14, 0, 14)

            CircleCorner.CornerRadius = UDim.new(3434, 8)
            CircleCorner.Name = "CircleCorner"
            CircleCorner.Parent = Circle

            Title_2.Name = "Title"
            Title_2.Parent = Slider
            Title_2.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
            Title_2.BackgroundTransparency = 1.000
            Title_2.Position = UDim2.new(0.94626379, 0, 0, 0)
            Title_2.Size = UDim2.new(0, 25, 0, 16)
            Title_2.Font = Enum.Font.GothamSemibold
            Title_2.Text = minvalue.."/"..maxvalue
            Title_2.TextColor3 = Color3.fromRGB(255, 255, 255)
            Title_2.TextSize = 13.000
            Title_2.TextTransparency = 0.470
            Title_2.TextXAlignment = Enum.TextXAlignment.Right
            local mouse = game.Players.LocalPlayer:GetMouse()
            local uis = game:GetService("UserInputService")
            local Value;
            local dragging = false 

            local function slide(input)
                local pos = UDim2.new(math.clamp((input.Position.X - Outer.AbsolutePosition.X) / Outer.AbsoluteSize.X, 0, 1), 0, 0, 7)
                Inner:TweenSize(pos, Enum.EasingDirection.Out, Enum.EasingStyle.Quart, 0.5, true)
                local value = math.floor(((pos.X.Scale * maxvalue) / maxvalue) * (maxvalue - minvalue) + minvalue)
                Title_2.Text = tostring(value) .. "/" .. maxvalue
                callback(value)
            end

            Outer.InputBegan:Connect(function(input)
                if input.UserInputType == Enum.UserInputType.MouseButton1 then
                    slide(input)
                    dragging = true
                end
            end)

            Outer.InputEnded:Connect(function(input)
                if input.UserInputType == Enum.UserInputType.MouseButton1 then
                    dragging = false
                end
            end)

            uis.InputChanged:Connect(function(input)
                if dragging and input.UserInputType == Enum.UserInputType.MouseMovement then
                    slide(input)
                end
            end)
            Inner.Size = UDim2.new((def or 0) / maxvalue, 0, 0, 7)
            Title_2.Text = tostring(def and math.floor((def / maxvalue) * (maxvalue - minvalue) + minvalue) or 0) .. '/' .. tostring(maxvalue)
            Outer.MouseEnter:Connect(function()
                TS:Create(Outer, TweenInfo.new(0.2, Enum.EasingStyle.Linear, Enum.EasingDirection.In), {
                    BackgroundTransparency = 0.5
                }):Play()
            end)
            Outer.MouseLeave:Connect(function()
                TS:Create(Outer, TweenInfo.new(0.2, Enum.EasingStyle.Linear, Enum.EasingDirection.In), {
                    BackgroundTransparency = 0.2
                }):Play()
            end)
        end

        function elements:DropDown(options)
            local drop_name = options.Text or 'Dropdown'
            local list = options.Options or {}
            local Callback = options.Callback or function() end

            local DropdownMenu = Instance.new("Frame")
            local Dropdown = Instance.new("TextButton")
            local DropdownCorner = Instance.new("UICorner")
            local Title = Instance.new("TextLabel")
            local ChooseAElement = Instance.new("Frame")
            local DropdownCorner_2 = Instance.new("UICorner")
            local ScrollingFrame = Instance.new("ScrollingFrame")

            local ElementsListing = Instance.new("UIListLayout")
            local Dropdown_2 = Instance.new("ImageLabel")
            
            --Properties:
            
            DropdownMenu.Name = "DropdownMenu"
            DropdownMenu.Parent = page
            DropdownMenu.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
            DropdownMenu.BackgroundTransparency = 1.000
            DropdownMenu.ClipsDescendants = true
            DropdownMenu.Position = UDim2.new(0, 0, 0.34080717, 0)
            DropdownMenu.Size = UDim2.new(0, 565, 0, 32)
            
            Dropdown.Name = "Dropdown"
            Dropdown.Parent = DropdownMenu
            Dropdown.BackgroundColor3 = Color3.fromRGB(45, 45, 45)
            Dropdown.BorderSizePixel = 0
            Dropdown.Position = UDim2.new(0, 0,0.01, 0)
            Dropdown.Size = UDim2.new(0, 565, 0, 29)
            Dropdown.AutoButtonColor = false
            Dropdown.Font = Enum.Font.GothamBold
            Dropdown.Text = ""
            Dropdown.TextColor3 = Color3.fromRGB(255, 255, 255)
            Dropdown.TextSize = 14.000

            Dropdown.MouseEnter:Connect(function()
                TS:Create(Dropdown, TweenInfo.new(0.2, Enum.EasingStyle.Linear, Enum.EasingDirection.In), {
                    BackgroundColor3 = Color3.fromRGB(65,65,65)
                }):Play()            
            end)

            Dropdown.MouseLeave:Connect(function()
                TS:Create(Dropdown, TweenInfo.new(0.2, Enum.EasingStyle.Linear, Enum.EasingDirection.In), {
                    BackgroundColor3 = Color3.fromRGB(45,45,45)
                }):Play()            
            end)

            local drop_Dropped = false

            Dropdown.MouseButton1Click:Connect(function()
                if drop_Dropped == false then
                    drop_Dropped = true
                    TS:Create(DropdownMenu, TweenInfo.new(0.2, Enum.EasingStyle.Linear, Enum.EasingDirection.In), {
                        Size = UDim2.new(0, 565, 0, 134)
                    }):Play()        
                    TS:Create(Dropdown_2, TweenInfo.new(0.2, Enum.EasingStyle.Linear, Enum.EasingDirection.In), {
                        Rotation = -90
                    }):Play()  
                    ScrollingFrame.CanvasPosition = Vector2.new(DropdownMenu.Size.X, DropdownMenu.Size.Y)
                else
                    drop_Dropped = false
                    TS:Create(DropdownMenu, TweenInfo.new(0.2, Enum.EasingStyle.Linear, Enum.EasingDirection.In), {
                        Size = UDim2.new(0, 565, 0, 32)
                    }):Play()          
                    TS:Create(Dropdown_2, TweenInfo.new(0.2, Enum.EasingStyle.Linear, Enum.EasingDirection.In), {
                        Rotation = 0
                    }):Play()  
                end
            end)
            
            DropdownCorner.CornerRadius = UDim.new(0, 4)
            DropdownCorner.Name = "DropdownCorner"
            DropdownCorner.Parent = Dropdown
            
            Title.Name = "Title"
            Title.Parent = Dropdown
            Title.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
            Title.BackgroundTransparency = 1.000
            Title.Position = UDim2.new(0.0123456791, 0, 0.241379321, 0)
            Title.Size = UDim2.new(0, 200, 0, 14)
            Title.Font = Enum.Font.GothamBold
            Title.Text = drop_name.." | nil"
            Title.TextColor3 = Color3.fromRGB(255, 255, 255)
            Title.TextSize = 14.000
            Title.TextXAlignment = Enum.TextXAlignment.Left
            
            ChooseAElement.Name = "ChooseAElement"
            ChooseAElement.Parent = Dropdown
            ChooseAElement.BackgroundColor3 = Color3.fromRGB(45, 45, 45)
            ChooseAElement.BorderSizePixel = 0
            ChooseAElement.ClipsDescendants = true
            ChooseAElement.Position = UDim2.new(0, 0, 1.17241383, 0)
            ChooseAElement.Size = UDim2.new(0, 565, 0, 96)
            
            DropdownCorner_2.CornerRadius = UDim.new(0, 4)
            DropdownCorner_2.Name = "DropdownCorner"
            DropdownCorner_2.Parent = ChooseAElement
            
            ScrollingFrame.Parent = ChooseAElement
            ScrollingFrame.Active = true
            ScrollingFrame.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
            ScrollingFrame.BackgroundTransparency = 1.010
            ScrollingFrame.BorderSizePixel = 0
            ScrollingFrame.Position = UDim2.new(0.012323726, 0, 0.0700000003, 0)
            ScrollingFrame.Size = UDim2.new(0, 552, 0, 87)
            ScrollingFrame.CanvasPosition = Vector2.new(0, 105)
            ScrollingFrame.ScrollBarThickness = 5
            

            
            ElementsListing.Name = "ElementsListing"
            ElementsListing.Parent = ScrollingFrame
            ElementsListing.SortOrder = Enum.SortOrder.LayoutOrder
            ElementsListing.Padding = UDim.new(0, 4)
            
            Dropdown_2.Name = "Dropdown"
            Dropdown_2.Parent = Dropdown
            Dropdown_2.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
            Dropdown_2.BackgroundTransparency = 1.000
            Dropdown_2.Position = UDim2.new(0.948027551, 0, 0.137931034, 0)
            Dropdown_2.Size = UDim2.new(0, 22, 0, 21)
            Dropdown_2.Image = "rbxassetid://7072706703"

            for i,v in pairs(options.Options) do
                local Element = Instance.new("TextButton")
                local ElementCorner = Instance.new("UICorner")

                Element.Name = "Element"
                Element.Parent = ScrollingFrame
                Element.BackgroundColor3 = Color3.fromRGB(39, 39, 39)
                Element.BorderSizePixel = 0
                Element.Position = UDim2.new(0, 0, 0.0156825278, 0)
                Element.Size = UDim2.new(0, 543, 0, 25)
                Element.AutoButtonColor = false
                Element.Font = Enum.Font.GothamBold
                Element.Text = v
                Element.TextColor3 = Color3.fromRGB(255, 255, 255)
                Element.TextSize = 12.000
                
                ElementCorner.CornerRadius = UDim.new(0, 4)
                ElementCorner.Name = "ElementCorner"
                ElementCorner.Parent = Element
                Element.MouseButton1Click:Connect(function()
                    
                    Callback(v)

                    drop_Dropped = false
                    TS:Create(Element, TweenInfo.new(0.08, Enum.EasingStyle.Linear, Enum.EasingDirection.In), {
                        BackgroundColor3 = Color3.fromRGB(180,180,180)
                    }):Play()  
                    wait(0.08)
                    TS:Create(Element, TweenInfo.new(0.08, Enum.EasingStyle.Linear, Enum.EasingDirection.In), {
                        BackgroundColor3 = Color3.fromRGB(39,39,39)
                    }):Play()  
                    TS:Create(DropdownMenu, TweenInfo.new(0.2, Enum.EasingStyle.Linear, Enum.EasingDirection.In), {
                        Size = UDim2.new(0, 565, 0, 32)
                    }):Play()          
                    TS:Create(Dropdown_2, TweenInfo.new(0.2, Enum.EasingStyle.Linear, Enum.EasingDirection.In), {
                        Rotation = 0
                    }):Play()  
                    Title.Text = drop_name.." | "..v
                end)
                Element.MouseEnter:Connect(function()
                    TS:Create(Element, TweenInfo.new(0.2, Enum.EasingStyle.Linear, Enum.EasingDirection.In), {
                        BackgroundColor3 = Color3.fromRGB(79, 79, 79)
                    }):Play()  
                end)
                Element.MouseLeave:Connect(function()
                    TS:Create(Element, TweenInfo.new(0.2, Enum.EasingStyle.Linear, Enum.EasingDirection.In), {
                        BackgroundColor3 = Color3.fromRGB(39,39,39)
                    }):Play()  
                end)
            end

            ElementsListing:GetPropertyChangedSignal("AbsoluteContentSize"):Connect(function()
                ScrollingFrame.CanvasSize = UDim2.new(0,0,0,ElementsListing.AbsoluteContentSize.Y) 
            end)
        end

        function elements:KeyBind(options)
            local title = options.Text or "Keybind Info"
            local binding = false
            local key = options.KeyPreset
            local Callback = options.Callback or function() end

            local KeyBind = Instance.new("TextButton")
            local KeyBindCorner = Instance.new("UICorner")
            local ActualKeybindBox = Instance.new("Frame")
            local ActualKeybindBoxCorner = Instance.new("UICorner")
            local TextLabel = Instance.new("TextLabel")
            local TextLabel_2 = Instance.new("TextLabel")

            --Properties:

            KeyBind.Name = "KeyBind"
            KeyBind.Parent = page
            KeyBind.BackgroundColor3 = Color3.fromRGB(45, 45, 45)
            KeyBind.Position = UDim2.new(0, 0, 0.520179391, 0)
            KeyBind.Size = UDim2.new(0, 563, 0, 34)
            KeyBind.AutoButtonColor = false
            KeyBind.Font = Enum.Font.SourceSans
            KeyBind.Text = ""
            KeyBind.TextColor3 = Color3.fromRGB(0, 0, 0)
            KeyBind.TextSize = 14.000

            KeyBindCorner.CornerRadius = UDim.new(0, 4)
            KeyBindCorner.Name = "KeyBindCorner"
            KeyBindCorner.Parent = KeyBind

            ActualKeybindBox.Name = "ActualKeybindBox"
            ActualKeybindBox.Parent = KeyBind
            ActualKeybindBox.BackgroundColor3 = Color3.fromRGB(0, 0, 0)
            ActualKeybindBox.BackgroundTransparency = 0.800
            ActualKeybindBox.Position = UDim2.new(0.928952157, 0, 0.117647059, 0)
            ActualKeybindBox.Size = UDim2.new(0, 34, 0, 25)

            ActualKeybindBoxCorner.CornerRadius = UDim.new(0, 4)
            ActualKeybindBoxCorner.Name = "ActualKeybindBoxCorner"
            ActualKeybindBoxCorner.Parent = ActualKeybindBox

            TextLabel.Parent = ActualKeybindBox
            TextLabel.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
            TextLabel.BackgroundTransparency = 1.000
            TextLabel.Position = UDim2.new(0, 0, -0.00235351571, 0)
            TextLabel.Size = UDim2.new(0, 34, 0, 25)
            TextLabel.Font = Enum.Font.GothamSemibold
            TextLabel.Text = "..."
            TextLabel.TextColor3 = Color3.fromRGB(255, 255, 255)
            TextLabel.TextSize = 14.000

            TextLabel_2.Parent = KeyBind
            TextLabel_2.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
            TextLabel_2.BackgroundTransparency = 1.000
            TextLabel_2.Position = UDim2.new(0.0124333929, 0, 0.117647059, 0)
            TextLabel_2.Size = UDim2.new(0, 508, 0, 25)
            TextLabel_2.Font = Enum.Font.GothamSemibold
            TextLabel_2.Text = "KeyBind Info"
            TextLabel_2.TextColor3 = Color3.fromRGB(255, 255, 255)
            TextLabel_2.TextSize = 14.000
            TextLabel_2.TextXAlignment = Enum.TextXAlignment.Left
            KeyBind.MouseButton1Click:Connect(function()
                TextLabel.Text = "..."
                binding = true
                local inputWait = game:GetService("UserInputService").InputBegan:wait()
                if inputWait.KeyCode.Name ~= "Unknown" then
                    TextLabel.Text = inputWait.KeyCode.Name
                    key = inputWait.KeyCode.Name
                    binding = false
                else
                    binding = false
                end
                game:GetService("UserInputService").InputBegan:connect(
                    function(current, pressed)
                        if not pressed then
                            if current.KeyCode.Name == key and binding == false then
                                pcall(Callback)
                            end
                        end
                    end
                    )
            end)
        end

        return elements
    end

    return tabs
end

return windows
