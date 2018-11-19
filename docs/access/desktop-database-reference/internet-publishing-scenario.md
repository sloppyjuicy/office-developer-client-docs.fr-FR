---
title: Scénario de publication Internet
TOCTitle: Internet publishing scenario
ms:assetid: 25a3fa8b-86ec-9e72-5e62-bf0d849479b7
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249024(v=office.15)
ms:contentKeyID: 48543790
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 1f481c4bc5cf11f9345458b3859c099b40a79885
ms.sourcegitcommit: 45feafb3b55de0402dddf5548c0c1c43a0eabafd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/07/2018
ms.locfileid: "26026448"
---
# <a name="internet-publishing-scenario"></a>Scénario de publication Internet

**S’applique à**: Access 2013, Office 2013

Cet exemple de code illustre la façon dont ADO doit être utilisé avec le fournisseur Microsoft OLE DB pour la publication Internet. Ce scénario consiste à créer une application Visual Basic qui utilise des objets **Recordset**, **Record** et **Stream** pour afficher le contenu des ressources publiées à l'aide du fournisseur de la publication Internet.

La création de ce scénario passe par l'exécution des étapes suivantes : 

1. Configurer le projet Visual Basic.
2. Initialiser la zone de liste principale.
3. Remplir la zone de liste de champs.
4. Remplir la zone de texte Details.

## <a name="step-1-set-up-the-visual-basic-project"></a>Étape 1 : Configurer le projet Visual Basic

Dans ce scénario, vous êtes censé avoir installé sur votre système Microsoft Visual Basic version 6.0 ou ultérieure, ADO version 2.5 ou ultérieure, et le fournisseur Microsoft OLE DB pour la publication Internet.

### <a name="create-an-ado-project"></a>Créer un projet ADO

1.  Dans Microsoft Visual Basic, créez un nouveau projet EXE standard.

2.  Dans le menu **Projet**, choisissez **Références**.

3.  Sélectionnez **Microsoft ActiveX Data Objects 2.5 Library**, puis cliquez sur **OK**.

### <a name="insert-controls-on-the-main-form"></a>Insérer des contrôles dans le formulaire principal

1.  Ajoutez un contrôle ListBox à Form1. Sa propriété **Name** la valeur **lstMain**.

2.  Ajoutez un autre contrôle ListBox à Form1. **Valeur lstDetails**, définissez sa propriété **Name** .

3.  Ajoutez un contrôle TextBox à Form1. Sa propriété **Name** la valeur **txtDetails**.

## <a name="step-2-initialize-the-main-list-box"></a>Étape 2 : Initialiser la zone de liste principale

### <a name="declare-global-record-and-recordset-objects"></a>Déclarer les objets Record et Recordset globaux

- Insérez le code suivant dans (Général) (Déclarations) pour Form1 :
    
   ```vb 
     
    Option Explicit 
    Dim grec As Record 
    Dim grs As Recordset 
   ```
    
   Ce code déclare des références pour les objets globaux **Record** et **Recordset** qui seront utilisés par la suite dans ce scénario.

### <a name="connect-to-a-url-and-populate-lstmain"></a>Se connecter à une URL et remplir lstMain

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
    
   Ce code instancie les objets **Record** et **Recordset** globaux. L' **enregistrement** `grec` est ouvert avec l’URL définie comme **ActiveConnection**. Si l'URL existe, elle est ouverte ; si elle n'existe pas encore, elle est créée. 
   
   Notez que vous devez remplacer `https://servername/foldername/` avec une URL valide de votre environnement. 
   
   Le **jeu d’enregistrements** `grs` est ouvert sur les enfants de l' **enregistrement** `grec`. La valeur lstMain est puis rempli avec les noms de fichier des ressources publiées à l’URL.

## <a name="step-3-populate-the-fields-list-box"></a>Étape 3 : Remplir la zone de liste de champs

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

   Ce code déclare et instancie les objets **Record** et **Recordset** locaux `rec` et `rs`respectivement.

   La ligne correspondant à la ressource sélectionnée dans lstMain devient la ligne en cours de `grs`. Zone de liste **Details** est ensuite effacée et `rec` est ouvert avec la ligne active de `grs` comme source.

   Si la ressource est un enregistrement de collection (comme spécifié par **RecordType**), le **jeu d’enregistrements** de local `rs` est ouvert sur les enfants de `rec`. lstDetails est ensuite rempli avec les valeurs des lignes de `rs`.

   Si la ressource est un enregistrement simple, `recFields` est appelée. Pour plus d’informations sur `recFields`, consultez l’étape suivante.

   Si la ressource est un document structuré, aucun code n'est implémenté.

## <a name="step-4-populate-the-details-text-box"></a>Étape 4 : Remplir la zone de texte Details

- Créer une nouvelle sous-routine nommée `recFields` et insérez le code suivant :

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

   Ce code remplit lstDetails avec les champs et les valeurs de l’enregistrement simple transmis à `recFields`. Si la ressource est un fichier texte, un objet **Stream** de type texte est ouvert à partir de l'enregistrement de la ressource. Le code détermine si le jeu de caractères est ASCII et copie le contenu du **flux** dans `txtDetails`.

