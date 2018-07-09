---
title: Journal des valeurs à un champ pour le débogage
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 5874dc28-1b10-48a3-8287-9474db0b7435
description: Lors du débogage d'un modèle de formulaire InfoPath, il est souvent utile de noter directement les valeurs dans un champ du formulaire pour créer un enregistrement des données de débogage au cours d'une session de test du formulaire. Les procédures qui suivent expliquent comment créer un champ à plusieurs lignes et comment ajouter des fonctions d'assistance au code du formulaire pour permettre l'enregistrement des données de débogage dans ce champ.
ms.openlocfilehash: f763e6b5d14fe5a5b4d9218af4acd0bc05a242af
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19782375"
---
# <a name="log-values-to-a-field-for-debugging"></a><span data-ttu-id="45b1f-104">Journal des valeurs à un champ pour le débogage</span><span class="sxs-lookup"><span data-stu-id="45b1f-104">Log values to a field for debugging</span></span>

<span data-ttu-id="45b1f-p102">Lors du débogage d'un modèle de formulaire InfoPath, il est souvent utile de noter directement les valeurs dans un champ du formulaire pour créer un enregistrement des données de débogage au cours d'une session de test du formulaire. Les procédures qui suivent expliquent comment créer un champ à plusieurs lignes et comment ajouter des fonctions d'assistance au code du formulaire pour permettre l'enregistrement des données de débogage dans ce champ.</span><span class="sxs-lookup"><span data-stu-id="45b1f-p102">When debugging an InfoPath form template, it is often useful to log values directly into a field in the form to create a record of debug data during a session of testing the form. The following procedures show how to create a multi-line field, and then add helper functions to the form code that enable you log debug data into that field.</span></span>
  
## <a name="create-a-multi-line-text-field"></a><span data-ttu-id="45b1f-107">Créer un champ de texte multilignes</span><span class="sxs-lookup"><span data-stu-id="45b1f-107">Create a multi-line text field</span></span>

1. <span data-ttu-id="45b1f-108">Ajouter un contrôle **Zone de texte** au formulaire, puis redimensionnez-le pour qu'il puisse contenir plusieurs lignes.</span><span class="sxs-lookup"><span data-stu-id="45b1f-108">Add a **Text Box** control to the form, and then resize it so that it can display multiple lines.</span></span> 
    
2. <span data-ttu-id="45b1f-109">Cliquez avec le bouton droit dans la zone de texte, cliquez sur **Propriétés de la zone de texte**, puis activez la case à cocher **Multiligne** dans l'onglet **Affichage**.</span><span class="sxs-lookup"><span data-stu-id="45b1f-109">Right-click the text box, click **Text Box Properties**, and then click the **Multi-line** check box on the **Display** tab.</span></span> 
    
## <a name="add-helper-functions-to-log-debug-information-to-the-field"></a><span data-ttu-id="45b1f-110">Ajouter des fonctions d’assistance pour enregistrer les informations de débogage dans le champ</span><span class="sxs-lookup"><span data-stu-id="45b1f-110">Add helper functions to log debug information to the field</span></span>

1. <span data-ttu-id="45b1f-111">Dans l'onglet **Développeur**, cliquez sur **Éditeur de code**, puis enregistrez le modèle de formulaire si vous y êtes invité.</span><span class="sxs-lookup"><span data-stu-id="45b1f-111">On the **Developer** tab, click **Code Editor**, and then save the form template if you are prompted.</span></span>
    
2. <span data-ttu-id="45b1f-112">Dans l'éditeur de code, ajoutez les trois fonctions d'assistance à la classe publique dans le fichier de code du formulaire.</span><span class="sxs-lookup"><span data-stu-id="45b1f-112">In the Code Editor, add the following three helper functions to the public class in the form code file.</span></span>
    
   > [!IMPORTANT]
   > <span data-ttu-id="45b1f-113">Assurez-vous de mettre à jour la valeur de la variable  `debugFieldXpath` dans la fonction  `AddToDebugField` pour qu'elle contienne la bonne expression XPath pour le champ lié au contrôle créé dans la première procédure.</span><span class="sxs-lookup"><span data-stu-id="45b1f-113">Make sure that you update the value set for the  `debugFieldXpath` variable in the  `AddToDebugField` function to the correct XPath expression for the field bound to the control that you created in the first procedure.</span></span> 
  
    ```cs
        private void AddToDebugField(string valueToAdd)
        {
            // Update the value of debugFieldXpath to the XPath of the
            // multi-line field where you want to log debug information.
            string debugFieldXpath = "/my:myFields/my:field1";
            string headerLine = "----------------- " + DateTime.Now + 
                " -----------------" + "\r\n";
            SetDebugFieldValue(debugFieldXpath, headerLine + valueToAdd + 
                "\r\n" + GetDebugFieldValue(debugFieldXpath));
        }
        private string GetDebugFieldValue(string xpath)
        {
            return this.CreateNavigator().SelectSingleNode(xpath, 
                this.NamespaceManager).Value;
        }
        private void SetDebugFieldValue(string xpath, string value)
        {
            this.CreateNavigator().SelectSingleNode(xpath, 
                this.NamespaceManager).SetValue(value);
        }
    ```

    ```vb
        Private Sub AddToDebugField(ByVal valueToAdd As String)
            ' Update the value of debugFieldXpath to the XPath of the 
            ' multi-line field where you want to log debug information.
            Dim debugFieldXpath As String = "/my:myFields/my:field1"
            Dim headerLine As String = "----------------- " _
                &amp; DateTime.Now &amp; " -----------------" &amp; vbCrLf
            SetDebugFieldValue(debugFieldXpath, (headerLine &amp; valueToAdd &amp; vbCrLf) _
                &amp; GetDebugFieldValue(debugFieldXpath))
        End Sub
        Private Function GetDebugFieldValue(ByVal xpath As String) As String
            Return Me.CreateNavigator().SelectSingleNode(xpath, _
                Me.NamespaceManager).Value
        End Function
        Private Sub SetDebugFieldValue(ByVal xpath As String, ByVal value As String)
            Me.CreateNavigator().SelectSingleNode(xpath, _
                Me.NamespaceManager).SetValue(value)
        End Sub
    ```

> [!NOTE] 
> <span data-ttu-id="45b1f-114">Lorsque vous utilisez Visual Basic, ajoutez `Imports Microsoft.VisualBasic.Constants` aux directives en haut du fichier de code de formulaire.</span><span class="sxs-lookup"><span data-stu-id="45b1f-114">When using Visual Basic, add  `Imports Microsoft.VisualBasic.Constants` to the directives at the top of the form code file.</span></span> 
  
## <a name="test-the-addtodebugfield-function"></a><span data-ttu-id="45b1f-115">Tester la fonction addtodebugfield :</span><span class="sxs-lookup"><span data-stu-id="45b1f-115">Test the AddToDebugField function</span></span>

1. <span data-ttu-id="45b1f-116">Dans l'onglet **Développeur**, cliquez sur **Événement Chargement en cours (Loading)**, puis ajoutez la ligne de code suivante au gestionnaire d'événement.</span><span class="sxs-lookup"><span data-stu-id="45b1f-116">On the **Developer** tab, click **Loading Event**, and then add the following line of code to the event handler.</span></span>
    
   ```cs
    AddToDebugField("Form loaded");
   ```

   ```vb
    AddToDebugField("Form loaded")
   ```

2. <span data-ttu-id="45b1f-117">Dans l'onglet **Développeur**, cliquez sur **Événement Vue modifiée (ViewSwitched)**, puis ajoutez la ligne de code suivante au gestionnaire d'événement.</span><span class="sxs-lookup"><span data-stu-id="45b1f-117">On the **Developer** tab, click **View Switched Event**, and then add the following line of code to the event handler.</span></span>
    
   ```cs
    AddToDebugField("View switched: " + this.CurrentView.ViewInfo.Name);
   ```

   ```vb
    AddToDebugField("View switched: " &amp; Me.CurrentView.ViewInfo.Name)
   ```

3. <span data-ttu-id="45b1f-118">Dans l'onglet **Accueil**, cliquez sur **Aperçu**.</span><span class="sxs-lookup"><span data-stu-id="45b1f-118">On the **Home** tab, click **Preview**.</span></span>
    
   <span data-ttu-id="45b1f-p103">Le champ de débogage doit afficher deux entrées : une indiquant que le formulaire est chargé et l'autre indiquant le nom de la vue. Ces exemples utilisent des gestionnaires d'événements pour les événements qui se produisent à l'ouverture du formulaire. Cependant, une fois le formulaire chargé, vous pouvez appeler la fonction  `AddToDebugField` à partir d'autres gestionnaires d'événements en plus du code qui s'exécute dans le contexte du formulaire.</span><span class="sxs-lookup"><span data-stu-id="45b1f-p103">The debug field should display two entries: one indicating that the form is loaded, and another indicating the name of the view. These examples use event handlers for events that occur as the form is opened. However, after the form is loaded, you can call the  `AddToDebugField` function from other event handlers in addition to any other code running in the context of the form.</span></span> 
  

