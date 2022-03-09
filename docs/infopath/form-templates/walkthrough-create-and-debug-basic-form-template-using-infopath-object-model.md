---
title: 'Walkthrough: Create and debug a basic form template using the InfoPath object model'
manager: soliver
ms.date: 01/13/2015
ms.audience: Developer
keywords:
- form templates [infopath 2007], walkthroughs,form templates [InfoPath 2007], creating InfoPath 2003-compatible,InfoPath 2003-compatible form templates, walkthroughs
ms.localizationpriority: medium
ms.assetid: 7658705f-c062-49a1-bea6-837737df2425
description: Cette rubrique fournit une procédure pas à pas de création d’un modèle de formulaire InfoPath avec code géré de base qui fonctionne avec le modèle objet compatible InfoPath 2003 fourni par Microsoft. Office. Espace de noms Interop.InfoPath.SemiTrust.
ms.openlocfilehash: eb4d3669eb71f3beaca897268d3e6d92a02df41c
ms.sourcegitcommit: 518845d053a009b11c8d907a33822161c0b6bc96
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/08/2022
ms.locfileid: "63375705"
---
# <a name="walkthrough-create-and-debug-a-basic-form-template-using-the-infopath-object-model"></a>Walkthrough: Create and debug a basic form template using the InfoPath object model

Cette rubrique fournit une procédure pas à pas de création d’un modèle de formulaire InfoPath avec code géré de base qui fonctionne avec le modèle objet compatible InfoPath 2003 fourni par [Microsoft.Office. Espace de noms Interop.InfoPath.SemiTrust](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.aspx).
  
## <a name="hello-world"></a>Hello World

Dans l’exemple suivant, vous allez apprendre à afficher une boîte de dialogue d’alerte simple à l’aide de la méthode [Alert](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UI2.Alert.aspx) du modèle objet compatible InfoPath 2003.
  
### <a name="create-a-new-infopath-form-template-that-works-with-the-infopath-2003-compatible-object-model"></a>Création d'un nouveau modèle de formulaire InfoPath qui fonctionne avec le modèle objet compatible InfoPath 2003

1. Créez un modèle de formulaire qui fonctionne avec le modèle objet compatible InfoPath 2003, comme décrit dans Créer un modèle de formulaire à l’aide du modèle objet [InfoPath 2003](how-to-create-a-form-template-using-the-infopath-2003-object-model.md).

2. Appelez le projet de modèle de formulaire HelloWorld et enregistrez-le.

   Le système de projet crée les fichiers de code et de projet, puis ouvre un modèle de formulaire vierge dans InfoPath en mode Création. Vous pouvez alors ajouter des gestionnaires d'événements.

### <a name="add-a-button-with-an-onclick-event-handler"></a>Ajout d'un bouton avec un gestionnaire d'événements OnClick

1. Dans la section **Contrôles** de l'onglet **Accueil**, cliquez sur le contrôle **Bouton** pour l'insérer dans la vue.

2. Cliquez avec le bouton droit sur le contrôle, puis cliquez sur **Propriétés du bouton**.

3. Modifiez **l’étiquette en** Alerte.

4. Modifiez **l’ID en** AlertID.

5. Cliquez sur **Modifier le code du formulaire**.

   Un squelette de handler d’événements pour l’événement [OnClick](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._ButtonEventSink_Event.OnClick.aspx) est créé et le focus passe à l’éditeur de code dans Visual Studio 2012. Pour plus d’informations sur l’utilisation des handlers d’événements, voir [Add an Event Handler Using the InfoPath 2003 Object Model](how-to-add-an-event-handler-using-the-infopath-2003-object-model.md).

   Vous pouvez maintenant ajouter du code de formulaire au gestionnaire d'événements du bouton.

### <a name="add-form-code-to-the-event-handler"></a>Ajout de code de formulaire au gestionnaire d'événements

1. Dans le gestionnaire d'événements **OnClick**, tapez le code suivant :

   ```cs
    thisXDocument.UI.Alert("Hello World!");
   ```

   ```vb
    thisXDocument.UI.Alert("Hello World!")
   ```

   Notez qu'une liste déroulante Microsoft IntelliSense s'affiche chaque fois que vous entrez un point dans la ligne de code. Le gestionnaire d'événements entier devrait ressembler à ce qui suit :

   ```cs
    [InfoPathEventHandler(MatchPath="AlertID", EventType=InfoPathEventType.OnClick)]
    public void AlertID_OnClick(DocActionEvent e)
    {
        thisXDocument.UI.Alert("Hello World!");
    }
   ```

   ```vb
    <InfoPathEventHandler(MatchPath:="AlertID", EventType:=InfoPathEventType.OnClick)>
    Public Sub AlertID_OnClick(ByVal e As DocActionEvent)
        thisXDocument.UI.Alert("Hello World!")
    End Sub
   ```

   > [!NOTE]
   > Au lieu d'employer la méthode **Alert**, vous pouvez utiliser la méthode **MessageBox.Show** de l'espace de noms **System.Windows.Forms** pour afficher un message. Pour ce faire, vous devez ajouter une référence au système. Windows. Assembly de formulaires`using System.Windows.Forms;`, ajout `Imports System.Windows.Forms` ou ajout aux directives au début de votre fichier de code, puis tapez une ligne de code telle que la suivante :`MessageBox.Show("Hello World!); or MessageBox.Show("Hello World!)`
  
2. Basculez dans la fenêtre du mode Création d'InfoPath, puis cliquez sur le bouton **Aperçu** sous l'onglet **Accueil**.

3. Dans la fenêtre **Aperçu**, cliquez sur le bouton **Alerte**.

   Un message s'affiche avec le texte « Hello World! ».

   La procédure suivante illustre l'ajout de points d'arrêt pour le débogage dans le code de votre formulaire.

### <a name="debug-form-code"></a>Débogage de code de formulaire

1. Dans l'Éditeur de code, cliquez sur la barre grise à droite de la ligne :

   ```cs
    thisXDocument.UI.Alert("Hello World!");
   ```

   ```vb
    thisXDocument.UI.Alert("Hello World!")
   ```

   Un cercle rouge s'affiche et la ligne de code est mise en surbrillance pour indiquer que l'exécution s'interrompra sur ce point d'arrêt.

2. Dans le menu **Débogage**, cliquez sur **Démarrer le débogage** ou appuyez sur F5.

3. Dans la fenêtre **Aperçu** d'InfoPath, cliquez sur le bouton **Alerte**.

   Le focus bascule sur l'Éditeur de code et la ligne où se trouve le point d'arrêt est mise en surbrillance.

4. Dans le menu **Débogage**, cliquez sur **Pas à pas principal** (ou appuyez sur Maj+F8 pour continuer pas à pas dans le code).

   Le code de la méthode **Alert** s'exécute et l'alerte « Hello World! » s'affiche dans la fenêtre **Aperçu** d'InfoPath.

## <a name="getting-the-current-users-name"></a>Récupération du nom d'utilisateur actuel

Avec les classes .NET Framework, vous pouvez accéder aux fonctionnalités qui n'étaient pas facilement disponibles depuis un script. Dans cet exemple, vous allez apprendre comment utiliser les classes .NET Framework pour récupérer le nom de l'utilisateur actuel.
  
### <a name="add-an-onload-event-handler"></a>Ajout d'un gestionnaire d'événements OnLoad

1. Ouvrez le projet HelloWorld InfoPath que vous avez créé précédemment.

2. Sous l'onglet **Affichage**, cliquez sur **Afficher les champs**.

3. Cliquez avec le bouton droit sur le nœud **mesChamps**, puis cliquez sur **Ajouter**.

4. Dans **Nom**, tapez **employé**, puis cliquez sur **OK**.

5. Faites glisser le nœud **employé** dans la vue.

6. Sous l'onglet **Développeur**, cliquez sur **Événement Sur chargement (OnLoad)**.

   Cela crée un handler d’événements pour [l’événement OnLoad](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocumentEventSink2_Event.OnLoad.aspx) et le focus se déplace vers l’éditeur de code. Le code de ce gestionnaire d'événements sera appelé à chaque chargement du formulaire. La procédure suivante illustre l'ajout d'un code de formulaire qui récupère le nom de l'utilisateur et le place dans le gestionnaire d'événements.

### <a name="add-form-code"></a>Ajout de code de formulaire 

1. Dans le gestionnaire d'événements **OnLoad**, tapez le code suivant :

   ```cs
    // Store an XML DOM node as a local variable.
    IXMLDOMNode nodeEmployee = thisXDocument.DOM.selectSingleNode("my:myFields/my:employee");
    if(nodeEmployee != null)
    {
        if(nodeEmployee.text == "")
        {
        // If the employee name is blank when the form is loaded, 
        // populate the employee node with the current user name.
        nodeEmployee.text = System.Environment.UserName;
        }
    }
   ```

   ```vb
    // Store an XML DOM node as a local variable.
    Dim nodeEmployee As IXMLDOMNode
    nodeEmployee = thisXDocument.DOM.selectSingleNode("my:myFields/my:employee");
    If Not(nodeEmployee Is Nothing) Then
        If(nodeEmployee.text = "") Then
        // If the employee name is blank when the form is loaded, 
        // populate the employee node with the current user name.
        nodeEmployee.text = System.Environment.UserName
        End If
    End If
   ```

2. Compilez et affichez un aperçu du formulaire.

   La zone de texte employé doit maintenant contenir votre nom d'utilisateur.

Pour plus d’informations sur le déploiement d’un modèle de formulaire avec code géré, voir [Déployer des modèles de formulaire InfoPath avec code](how-to-deploy-infopath-form-templates-with-code.md). Pour plus d’informations sur le modèle objet InfoPath et les tâches de programmation courantes dans les modèles de formulaires avec code géré qui fonctionnent avec le modèle objet compatible InfoPath 2003, voir Présentation du modèle objet [InfoPath 2003](understanding-the-infopath-2003-object-model.md).
  
## <a name="see-also"></a>Voir aussi

- [Code d'initialisation et de nettoyage à l'aide du modèle objet InfoPath 2003](initialization-and-clean-up-code-using-infopath-2003-object-model.md)
- [Modèles objet compatibles avec InfoPath 2003](infopath-2003-compatible-object-models.md)
- [Ajouter un handler d’événements à l’aide du modèle objet InfoPath 2003](how-to-add-an-event-handler-using-the-infopath-2003-object-model.md)
