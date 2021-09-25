---
title: Enregistrement des valeurs dans un champ pour réaliser le débogage
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
ms.assetid: 5874dc28-1b10-48a3-8287-9474db0b7435
description: Lors du débogage d'un modèle de formulaire InfoPath, il est souvent utile de noter directement les valeurs dans un champ du formulaire pour créer un enregistrement des données de débogage au cours d'une session de test du formulaire. Les procédures qui suivent expliquent comment créer un champ à plusieurs lignes et comment ajouter des fonctions d'assistance au code du formulaire pour permettre l'enregistrement des données de débogage dans ce champ.
ms.openlocfilehash: e971ecc6a82cb5a0b5594a458544fe619c27abea
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59564616"
---
# <a name="log-values-to-a-field-for-debugging"></a>Enregistrement des valeurs dans un champ pour réaliser le débogage

Lors du débogage d'un modèle de formulaire InfoPath, il est souvent utile de noter directement les valeurs dans un champ du formulaire pour créer un enregistrement des données de débogage au cours d'une session de test du formulaire. Les procédures qui suivent expliquent comment créer un champ à plusieurs lignes et comment ajouter des fonctions d'assistance au code du formulaire pour permettre l'enregistrement des données de débogage dans ce champ.
  
## <a name="create-a-multi-line-text-field"></a>Créer un champ de texte multi-lignes

1. Ajouter un contrôle **Zone de texte** au formulaire, puis redimensionnez-le pour qu'il puisse contenir plusieurs lignes. 
    
2. Cliquez avec le bouton droit dans la zone de texte, cliquez sur **Propriétés de la zone de texte**, puis activez la case à cocher **Multiligne** dans l'onglet **Affichage**. 
    
## <a name="add-helper-functions-to-log-debug-information-to-the-field"></a>Ajouter des fonctions d’aide pour enregistrer les informations de débogage dans le champ

1. Dans l'onglet **Développeur**, cliquez sur **Éditeur de code**, puis enregistrez le modèle de formulaire si vous y êtes invité.
    
2. Dans l'éditeur de code, ajoutez les trois fonctions d'assistance à la classe publique dans le fichier de code du formulaire.
    
   > [!IMPORTANT]
   > [!IMPORTANTE] Assurez-vous de mettre à jour la valeur de la variable  `debugFieldXpath` dans la fonction  `AddToDebugField` pour qu'elle contienne la bonne expression XPath pour le champ lié au contrôle créé dans la première procédure. 
  
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
> Lorsque vous utilisez Visual Basic, ajoutez-les aux directives en haut du fichier de `Imports Microsoft.VisualBasic.Constants` code du formulaire. 
  
## <a name="test-the-addtodebugfield-function"></a>Tester la fonction AddToDebugField

1. Dans l'onglet **Développeur**, cliquez sur **Événement Chargement en cours (Loading)**, puis ajoutez la ligne de code suivante au gestionnaire d'événement.
    
   ```cs
    AddToDebugField("Form loaded");
   ```

   ```vb
    AddToDebugField("Form loaded")
   ```

2. Dans l'onglet **Développeur**, cliquez sur **Événement Vue modifiée (ViewSwitched)**, puis ajoutez la ligne de code suivante au gestionnaire d'événement.
    
   ```cs
    AddToDebugField("View switched: " + this.CurrentView.ViewInfo.Name);
   ```

   ```vb
    AddToDebugField("View switched: " &amp; Me.CurrentView.ViewInfo.Name)
   ```

3. Dans l'onglet **Accueil**, cliquez sur **Aperçu**.
    
   Le champ de débogage doit afficher deux entrées : une indiquant que le formulaire est chargé et l'autre indiquant le nom de la vue. Ces exemples utilisent des gestionnaires d'événements pour les événements qui se produisent à l'ouverture du formulaire. Cependant, une fois le formulaire chargé, vous pouvez appeler la fonction  `AddToDebugField` à partir d'autres gestionnaires d'événements en plus du code qui s'exécute dans le contexte du formulaire. 
  

