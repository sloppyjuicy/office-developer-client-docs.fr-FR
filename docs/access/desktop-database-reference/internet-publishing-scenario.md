---
title: Scénario de publication Internet
TOCTitle: Internet publishing scenario
ms:assetid: 25a3fa8b-86ec-9e72-5e62-bf0d849479b7
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249024(v=office.15)
ms:contentKeyID: 48543790
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 0f28b14f3eaf6792a74ef0967d698d5a3914955a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32291271"
---
# <a name="internet-publishing-scenario"></a>Scénario de publication Internet

**S’applique à** : Access 2013, Office 2013

Cet exemple de code illustre la façon dont ADO doit être utilisé avec le fournisseur Microsoft OLE DB pour la publication Internet. Ce scénario consiste à créer une application Visual Basic qui utilise des objets **Recordset**, **Record** et **Stream** pour afficher le contenu des ressources publiées à l'aide du fournisseur de la publication Internet.

La création de ce scénario passe par l'exécution des étapes suivantes : 

1. Configurer le projet Visual Basic projet.
2. Initialiser la zone de liste Principale.
3. Remplir la zone de liste Champs.
4. Remplir la zone de texte Détails.

## <a name="step-1-set-up-the-visual-basic-project"></a>Étape 1 : Configurer le projet Visual Basic projet

Dans ce scénario, vous êtes censé avoir installé sur votre système Microsoft Visual Basic version 6.0 ou ultérieure, ADO version 2.5 ou ultérieure, et le fournisseur Microsoft OLE DB pour la publication Internet.

### <a name="create-an-ado-project"></a>Créer un projet ADO

1.  Dans Microsoft Visual Basic, créez un nouveau projet EXE standard.

2.  Dans le menu **Projet**, choisissez **Références**.

3.  Sélectionnez **Microsoft ActiveX Data Objects 2.5 Library,** puis cliquez sur **OK**.

### <a name="insert-controls-on-the-main-form"></a>Insérer des contrôles sur le formulaire principal

1.  Ajoutez un contrôle ListBox à Form1. Définissez **sa propriété Name** sur **lstMain**.

2.  Ajoutez un autre contrôle ListBox à Form1. Définissez **sa propriété Name** sur **lstDetails**.

3.  Ajoutez un contrôle TextBox à Form1. Définissez **sa propriété Name** sur **txtDetails**.

## <a name="step-2-initialize-the-main-list-box"></a>Étape 2 : Initialiser la zone de liste principale

### <a name="declare-global-record-and-recordset-objects"></a>Déclarer des objets Record et Recordset globaux

- Insérez le code suivant dans (Général) (Déclarations) pour Form1 :
    
   ```vb 
     
    Option Explicit 
    Dim grec As Record 
    Dim grs As Recordset 
   ```
    
   Ce code déclare des références pour les objets globaux **Record** et **Recordset** qui seront utilisés par la suite dans ce scénario.

### <a name="connect-to-a-url-and-populate-lstmain"></a>Connecter à une URL et remplir lstMain

- Insérez le code suivant dans le gestionnaire d'événements Form Load pour Form1 :
    
   ```vb 
     
    Private Sub Form_Load() 
        Set grec = New Record 
        Set grs = New Recordset 
        grec.Open "", "URL=https://servername/foldername/", , _ 
            adOpenIfExists Or adCreateCollection 
        Set grs = grec.GetChildren 
        While Not grs.EOF 
            lstMain.AddItem grs(0) 
            grs.MoveNext 
        Wend 
    End Sub 
   ```
    
   Ce code instancie les objets **Record** et **Recordset** globaux. **L’enregistrement** `grec` est ouvert avec une URL spécifiée comme **ActiveConnection**. Si l'URL existe, elle est ouverte ; si elle n'existe pas encore, elle est créée. 
   
   Notez que vous devez remplacer `https://servername/foldername/` par une URL valide de votre environnement. 
   
   Le **recordset** `grs` est ouvert sur les enfants de l’enregistrement  `grec` . Le lstMain est ensuite rempli avec les noms de fichiers des ressources publiées dans l’URL.

## <a name="step-3-populate-the-fields-list-box"></a>Étape 3 : Remplir la zone de liste Champs

- Insérez le code suivant dans le gestionnaire d'événements Click de lstMain :

   ```vb 
    
    Private Sub lstMain_Click() 
        Dim rec As Record 
        Dim rs As Recordset 
        Set rec = New Record 
        Set rs = New Recordset 
        grs.MoveFirst 
        grs.Move lstMain.ListIndex 
        lstDetails.Clear 
        rec.Open grs 
        Select Case rec.RecordType 
            Case adCollectionRecord: 
                Set rs = rec.GetChildren 
                While Not rs.EOF 
                    lstDetails.AddItem rs(0) 
                    rs.MoveNext 
                Wend 
            Case adSimpleRecord: 
                recFields rec, lstDetails, txtDetails 
                
            Case adStructDoc: 
        End Select 
        
    End Sub 
   ```

   Ce code déclare et ins instantie les objets **Record** et **Recordset** `rec` `rs` locaux, respectivement.

   La ligne correspondant à la ressource sélectionnée dans lstMain est la ligne actuelle de `grs` . La **zone de liste Détails** est ensuite effacée et ouverte avec la ligne actuelle de la `rec` `grs` source.

   Si la ressource est un enregistrement de collection (comme spécifié par **RecordType**), l’recordset local est ouvert sur  `rs` les enfants de `rec` . lstDetails est ensuite rempli avec les valeurs des lignes de `rs` .

   Si la ressource est un enregistrement simple, `recFields` elle est appelée. Pour plus d’informations `recFields` sur , voir l’étape suivante.

   Si la ressource est un document structuré, aucun code n'est implémenté.

## <a name="step-4-populate-the-details-text-box"></a>Étape 4 : Remplir la zone de texte Détails

- Créez une sous-routine nommée `recFields` et insérez le code suivant :

   ```vb 
    
    Sub recFields(r As Record, l As ListBox, t As TextBox) 
        Dim f As Field 
        Dim s As Stream 
        Set s = New Stream 
        Dim str As String 
        
        For Each f In r.Fields 
            l.AddItem f.Name & ": " & f.Value 
        Next 
        t.Text = "" 
        If r!RESOURCE_CONTENTCLASS = "text/plain" Then 
            s.Open r, adModeRead, adOpenStreamFromRecord 
            str = s.ReadText(1) 
            s.Position = 0 
            If Asc(Mid(str, 1, 1)) = 63 Then '//63 = "?" 
                s.Charset = "ascii" 
                s.Type = adTypeText 
            End If 
            t.Text = s.ReadText(adReadAll) 
        End If 
    End Sub 
   ```

   Ce code remplit lstDetails avec les champs et les valeurs de l’enregistrement simple passé à `recFields` . Si la ressource est un fichier texte, un objet **Stream** de type texte est ouvert à partir de l'enregistrement de la ressource. Le code détermine si le jeu de caractères est ASCII et copie le contenu **du flux** dans `txtDetails` .

