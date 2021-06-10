---
title: Container, objet (DAO)
TOCTitle: Container Object
ms:assetid: 22e487cd-e966-fe68-fff3-c680b460cbeb
ms:mtpsurl: https://msdn.microsoft.com/library/Ff191764(v=office.15)
ms:contentKeyID: 48543720
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: c9ebbeae35387f4fd59c39d4c20df6033edb06b0
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32295631"
---
# <a name="container-object-dao"></a>Container, objet (DAO)

**S’applique à** : Access 2013, Office 2013

Un objet **Container** regroupe des types d'objets **Document** similaires.

## <a name="remarks"></a>Remarques

Chaque objet **Database** comporte une collection **Containers** composée d'objets **Container** intégrés. Les applications peuvent définir leurs propres types de document et les conteneurs correspondants (bases de données de moteur de base de données Microsoft Access uniquement). Cependant, il peut arriver que ces objets ne soient pas toujours pris en charge dans DAO.

Certains de ces objets **Container** sont définis par le moteur de base de données Microsoft Access alors que les autres peuvent définis par d'autres applications. Le tableau ci-dessous répertorie le nom de chaque objet **Container** défini par le moteur de base de données Microsoft Access et indique le type d'informations qu'ils contiennent.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Nom du conteneur</p></th>
<th><p>Contient des informations sur</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>Databases</p></td>
<td><p>Bases de données enregistrées</p></td>
</tr>
<tr class="even">
<td><p>Tables</p></td>
<td><p>Tables et requêtes enregistrées</p></td>
</tr>
<tr class="odd">
<td><p>Relations</p></td>
<td><p>Relations enregistrées</p></td>
</tr>
</tbody>
</table>

> [!NOTE]
> [!REMARQUE] Ne confondez pas les objets **Container** répertoriés dans le tableau précédent avec les collections du même nom. L'objet **Container** des bases de données renvoie à tous les objets de base de données enregistrés, mais la collection **Databases** renvoie uniquement aux objets de base de données ouverts dans un espace de travail déterminé.

Chaque objet **Container** comporte une collection **Documents** qui contient des objets **Document** qui décrivent les instances des objets intégrés du type spécifié par l'objet **Container**. Généralement, vous utilisez un objet **Container** comme liaison intermédiaire vers les informations dans l'objet **Document**. Vous pouvez également utiliser la collection **Containers** pour définir la sécurité de tous les objets **Document** d'un type déterminé.

Avec un objet **Container** existant, vous pouvez :

- Utiliser la propriété **Name** pour renvoyer le nom prédéfini de l'objet **Container**.

- Utiliser la propriété **Owner** pour définir ou renvoyer le propriétaire de l'objet **Container**. Pour définir la propriété **Owner**, vous devez disposer de l'autorisation d'écrire pour l'objet **Container**, et vous devez définir la propriété sur le nom d'un objet **User** ou **Group** existant.

- Utiliser les propriétés **Permissions** et **UserName** pour définir les autorisations d'accès pour l'objet **Container**. Tout objet **Document** créé dans la collection **Documents** d'un objet **Container** hérite de ces paramètres d'autorisation d'accès.

Comme les objets **Container** sont intégrés, vous ne pouvez pas créer d'objets **Container** ou supprimer des objets Container existants.

Pour renvoyer à un objet **Container** dans une collection par son numéro ordinal ou par son paramètre de propriété **Name**, utilisez l'une des formes de syntaxe suivantes :

- **Conteneurs**(0)

- **Conteneurs**( »*nom*« )

-  \! Conteneurs \[ *name*\]

## <a name="example"></a>Exemple

Cet exemple énumère la collection **Containers** de la base de données Northwind et la collection **Properties** de chaque objet **Container** dans la collection.

```vb
    Sub ContainerObjectX() 
     
     Dim dbsNorthwind As Database 
     Dim ctrLoop As Container 
     Dim prpLoop As Property 
     
     Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     
     With dbsNorthwind 
     
     ' Enumerate Containers collection. 
     For Each ctrLoop In .Containers 
     Debug.Print "Properties of " & ctrLoop.Name _ 
     & " container" 
     
     ' Enumerate Properties collection of each 
     ' Container object. 
     For Each prpLoop In ctrLoop.Properties 
     Debug.Print " " & prpLoop.Name _ 
     & " = " prpLoop 
     Next prpLoop 
     
     Next ctrLoop 
     
     .Close 
     End With 
     
    End Sub
```
