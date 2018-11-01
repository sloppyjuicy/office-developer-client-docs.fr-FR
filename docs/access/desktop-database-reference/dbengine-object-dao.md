---
title: DBEngine Object (DAO)
TOCTitle: DBEngine Object
ms:assetid: ceaeb505-615e-37ba-4633-27240ef8c5de
ms:mtpsurl: https://msdn.microsoft.com/library/Ff834506(v=office.15)
ms:contentKeyID: 48547792
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 86c14ef0e9443965b2e80af329d4cca6023d1467
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25873628"
---
# <a name="dbengine-object-dao"></a>DBEngine Object (DAO)

**S’applique à**: Access 2013, Office 2013

L'objet **DBEngine** est l'objet de niveau supérieur dans le modèle objet DAO.

## <a name="remarks"></a>Remarques

L'objet **DBEngine** contient et contrôle tous les autres objets dans la hiérarchie des objets DAO. Vous ne pouvez pas créer d'autres objets **DBEngine** et l'objet **DBEngine** n'est pas un élément d'une collection.

Avec tous les types de base de données ou de connexion, vous pouvez :

  - Utiliser la propriété **Version** pour obtenir le numéro de version DAO.

  - Utiliser la propriété **LoginTimeout** pour obtenir ou définir le temps d'expiration de la connexion ODBC et la méthode **RegisterDatabase** pour fournir des informations ODBC au moteur de base de données Microsoft Access.

  - Utiliser les propriétés **DefaultPassword** et **DefaultUser** pour définir l'identification et le mot de passe utilisateur pour l'objet **Workspace** par défaut.

  - Utiliser la méthode **CreateWorkspace** pour créer un objet **Workspace**. Vous pouvez utiliser des arguments facultatifs pour remplacer les paramètres des propriétés **DefaultType**, **DefaultPassword** et **DefaultUser**.

  - Utiliser la méthode **OpenDatabase** pour ouvrir une base de données dans l'objet **Workspace** par défaut, et utiliser les méthodes **BeginTrans**, **Commit** et **Rollback** pour contrôler les transactions dans l'objet **Workspace** par défaut.

  - Utiliser la collection **Workspaces** pour référencer des objets **Workspace** spécifiques.

  - Utiliser la collection **Errors** pour examiner les détails des erreurs d'accès aux données.

D'autres propriétés et méthodes sont disponibles lorsque vous utilisez DAO avec le moteur de base de données Microsoft Access. Vous pouvez les utiliser pour contrôler le moteur de base de données Microsoft Access, manipuler ses propriétés, et effectuer des tâches sur des objets temporaires qui ne sont pas des éléments de collections. Par exemple, vous pouvez :

  - Utiliser la méthode **CreateDatabase** pour créer un objet **Database** de moteur de base de données Microsoft Access.

  - Utiliser la méthode **Idle** pour permettre au moteur de base de données Microsoft Access de terminer des tâches en attente.

  - Utiliser les méthodes **CompactDatabase** et **RepairDatabase** pour effectuer la maintenance des fichiers de base de données.

  - Utiliser les propriétés **IniPath** et **SystemDB** pour spécifier respectivement l'emplacement des informations de registre Windows du moteur de base de données Microsoft Access et celui du fichier d'informations de groupe de travail Microsoft Access. La méthode **SetOption** permet de remplacer les paramètres du registre Windows pour le moteur de base de données Microsoft Access.

Une fois que vous modifiez les paramètres des propriétés **DefaultType** et **IniPath**, seuls les objets **Workspace** suivants reflètent ces modifications.

Pour renvoyer à une collection qui appartient à l'objet **DBEngine**, ou pour renvoyer à une méthode ou à une propriété qui s'applique à cet objet, utilisez cette syntaxe :

\[**DBEngine**. \] \[collection | méthode | propriété\]

## <a name="example"></a>Exemple

Cet exemple énumère les collections de l'objet **DBEngine**.

```vb
    Sub DBEngineX() 
     
     Dim wrkLoop As Workspace 
     Dim prpLoop As Property 
     
     With DBEngine 
     Debug.Print "DBEngine Properties" 
     
     ' Enumerate Properties collection of DBEngine, 
     ' trapping for properties whose values are 
     ' invalid in this context. 
     For Each prpLoop In .Properties 
     On Error Resume Next 
     Debug.Print " " & prpLoop.Name & " = " _ 
     & prpLoop 
     On Error GoTo 0 
     Next prpLoop 
     
     Debug.Print "Workspaces collection of DBEngine" 
     
     ' Enumerate Workspaces collection of DBEngine. 
     For Each wrkLoop In .Workspaces 
     Debug.Print " " & wrkLoop.Name 
     
     ' Enumerate Properties collection of each 
     ' Workspace object, trapping for properties 
     ' whose values are invalid in this context. 
     For Each prpLoop In wrkLoop.Properties 
     On Error Resume Next 
     Debug.Print " " & prpLoop.Name & _ 
     " = " & prpLoop 
     On Error GoTo 0 
     Next prpLoop 
     
     Next wrkLoop 
     
     End With 
     
    End Sub
```
