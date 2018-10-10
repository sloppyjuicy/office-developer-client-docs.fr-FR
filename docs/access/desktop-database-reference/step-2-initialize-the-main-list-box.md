---
title: 'Étape 2 : initialiser la zone de liste principale'
TOCTitle: 'Step 2: Initialize the Main List Box'
ms:assetid: 81e4dcfd-6ee0-b5f9-9ea3-026c38c26bf0
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249562(v=office.15)
ms:contentKeyID: 48545967
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: f2b6b4d79262796aa8e9090d673a439a550f042c
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25471510"
---
# <a name="step-2-initialize-the-main-list-box"></a>Étape 2 : initialiser la zone de liste principale


**S’applique à**: Access 2013 | Office 2013

## <a name="step-2-initialize-the-main-list-box"></a>Étape 2 : initialiser la zone de liste principale

**Pour déclarer les objets Record et Recordset globaux**

  - Insérez le code suivant dans (Général) (Déclarations) pour Form1 :
    
    ```vb 
     
    Option Explicit 
    Dim grec As Record 
    Dim grs As Recordset 
    ```
    
    Ce code déclare des références pour les objets globaux **Record** et **Recordset** qui seront utilisés par la suite dans ce scénario.

**Pour se connecter à une URL et remplir lstMain**

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
    
    Ce code instancie les objets **Record** et **Recordset** globaux. L’objet **Record**, grec, est ouvert avec l’URL définie comme **ActiveConnection**. Si l'URL existe, elle est ouverte ; si elle n'existe pas encore, elle est créée. Notez que vous devez remplacer « https://servername/foldername/ » par une URL valide de votre environnement. L' **objet Recordset**, grs, est ouvert sur les enfants de l’objet **Record**, grec. lstMain est ensuite rempli avec les noms de fichier des ressources publiées au niveau de l'URL.

