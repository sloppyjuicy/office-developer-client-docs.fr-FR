---
title: Utilisation d'ADO avec Microsoft Visual Basic
TOCTitle: Using ADO with Microsoft Visual Basic
ms:assetid: 5e0fb2ec-42aa-e181-386f-099607ac7400
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249338(v=office.15)
ms:contentKeyID: 48545130
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 26eaa93a1abbb3778a2735d50dd5022edb3023d9
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32306222"
---
# <a name="using-ado-with-microsoft-visual-basic"></a>Utilisation d’ADO avec Microsoft Visual Basic

**S’applique à** : Access 2013, Office 2013

Configurer un projet ADO et écrire du code ADO sont des tâches similaires que vous utilisiez Visual Basic ou Visual Basic pour Applications. Cette rubrique explique comment utiliser ADO avec Visual Basic et Visual Basic pour Applications en relevant les différences qui existent selon le programme utilisé.

## <a name="referencing-the-ado-library"></a>Référencement de la bibliothèque ADO

La bibliothèque ADO doit être référencée par votre projet.

### <a name="to-reference-ado-from-microsoft-visual-basic"></a>Pour référencer la bibliothèque ADO à partir de Microsoft Visual Basic

1. Dans le menu **Projet** de Visual Basic, sélectionnez **Références...**.

2. Sélectionnez **Bibliothèque Microsoft ActiveX Data Objects x.x** dans la liste. Vérifiez que les bibliothèques suivantes sont au moins sélectionnées :
   
   - Visual Basic pour Applications
   - Objets et procédures d'exécution Visual Basic
   - Objets et procédures Visual Basic
   - OLE Automation

3. Cliquez sur **OK**.

ADO s'utilise aussi facilement avec Visual Basic pour Applications, via Microsoft Access par exemple.

### <a name="to-reference-ado-from-microsoft-access"></a>Pour référencer ADO à partir de Microsoft Access

1. Dans Microsoft Access, sélectionnez ou créez un module dans l'onglet **Modules** de la fenêtre **Base de données**.

2. Dans le menu **Outils**, cliquez sur **Références...**.

3. Sélectionnez **Bibliothèque Microsoft ActiveX Data Objects x.x** dans la liste. Vérifiez que les bibliothèques suivantes sont au moins sélectionnées :
    
   - Visual Basic pour Applications
   - Bibliothèque d'objets Microsoft Access 11.0 (ou version ultérieure)

4. Cliquez sur **OK**.

## <a name="creating-ado-objects-in-visual-basic"></a>Création d'objets ADO dans Visual Basic

Pour créer une variable Automation et une instance d'un objet pour cette variable, vous pouvez faire appel aux méthodes **Dim** ou **CreateObject**.

### <a name="dim"></a>Dim

Vous pouvez utiliser le mot-clé **New** avec la méthode **Dim** pour déclarer et instancier des objets ADO en une seule étape :

```vb 
 
Dim conn As New ADODB.Connection 
```

Alternately, the **Dim** statement declaration and object instantiation can also be two steps:

```vb 
 
Dim conn As ADODB.Connection 
Set conn = New ADODB.Connection 
```

> [!NOTE]
> Il n'est pas nécessaire d'utiliser explicitement le ProgID ADODB avec l'instruction **Dim** , en supposant que vous avez correctement référencé la bibliothèque ADO dans votre projet. Toutefois, son utilisation garantit l'absence de conflits de noms avec d'autres bibliothèques.
> 
> Par exemple, si vous référencez à des objets ADO et DAO dans le même projet, vous devez inclure un qualificatif afin de spécifier quel modèle objet utiliser lors de l'instanciation d'objets **Recordset** comme dans le code suivant :  
> 
> `Dim adoRS As ADODB.Recordset`  
>   
> `Dim daoRS As DAO.Recordset`

### <a name="createobject"></a>CreateObject

Avec la méthode **CreateObject**, la déclaration et l'instanciation d'objet doit se faire en deux étapes discrètes :

```vb 
 
Dim conn1 
Set conn1 = CreateObject("ADODB.Connection") As Object 
```

Les objets instanciés avec la méthode **CreateObject** sont à liaison tardive, ce qui signifie qu'ils ne sont pas fortement typés et leur exécution à partir de la ligne de commande est désactivée. Toutefois, cette méthode vous permet de ne pas référencer la bibliothèque ADO à partir de votre projet mais bien d'instancier des versions spécifiques des objets. Par exemple :

```vb 
 
Set conn1 = CreateObject("ADODB.Connection.2.0") As Object 
```

Vous pouvez également exécuter cette opération en définissant une référence spécifique à la bibliothèque de types ADO version 2.0 et en créant l'objet.

L'instanciation d'objets à l'aide de la méthode **CreateObject** est généralement plus lente qu'avec la déclaration **Dim**.

## <a name="handling-events"></a>Gestion des événements

Pour gérer les événements ADO en Microsoft Visual Basic, vous devez déclarer une variable de niveau module à l'aide du mot clé **WithEvents** . La variable ne peut être déclarée qu'au sein d'un module de classe et doit être déclarée au niveau du module. Pour plus d'informations sur la gestion des événements ADO, consultez le [chapitre 7: gestion des événements ADO](chapter-7-handling-ado-events.md).

## <a name="visual-basic-examples"></a>Exemples Visual Basic

De nombreux exemples Visual Basic sont inclus dans la documentation ADO. Pour plus d'informations, consultez la rubrique [exemples de code ADO en Microsoft Visual Basic](ado-code-examples-in-microsoft-visual-basic.md).

