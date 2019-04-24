---
title: Fields, collection
TOCTitle: The Fields Collection
ms:assetid: 3bda8e5d-eceb-9605-c4d7-c1f4cc00ce6b
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249154(v=office.15)
ms:contentKeyID: 48544297
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: ce08ac5952151471ce74afd9a8a49600d8e8f633
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32314132"
---
# <a name="fields-collection"></a>Fields, collection


**S’applique à** : Access 2013, Office 2013

La collection **Fields** est une des collections intrinsèques d'ADO. Une collection est un ensemble hiérarchique d'éléments qui peuvent être référencés en tant qu'unité.

La collection **Fields** contient un objet **Field** pour chaque champ (colonne) de l'objet **Recordset**. Comme toutes les collections ADO, elle possède les propriétés **Count** et **Item**, ainsi que les méthodes **Append** et **Refresh**. Notons également la présence des méthodes **CancelUpdate**, **Delete**, **Resync** et **Update**, non disponibles pour les autres collections ADO.

## <a name="examining-the-fields-collection"></a>Présentation de la collection Fields

Consider the **Fields** collection of the sample **Recordset** introduced in this chapter. The sample **Recordset** was derived from the SQL statement

```sql 
 
SELECT ProductID, ProductName, UnitPrice FROM Products WHERE CategoryID = 7 
```

Nous constatons donc que la collection **Fields** de l'objet **Recordset** contient trois champs.

```vb 
 
'BeginWalkFields 
 Dim objFields As ADODB.Fields 
 
 objRs.Open strSQL, strConnStr, adOpenForwardOnly, adLockReadOnly, adCmdText 
 
 Set objFields = objRs.Fields 
 
 For intLoop = 0 To (objFields.Count - 1) 
 Debug.Print objFields.Item(intLoop).Name 
 Next 
'EndWalkFields 
```

Ce code détermine simplement le nombre d'objets **Field** de la collection **Fields**, par l'intermédiaire de la propriété **Count**. Il parcourt la collection et renvoie la valeur de la propriété **Name** de chaque objet **Field**. Il existe bien d'autres propriétés **Field** qui permettent d'obtenir des informations concernant un champ. Pour plus d'informations sur les requêtes qu'il est possible d'exécuter sur un objet **Field**, consultez la rubrique [Field, objet](the-field-object.md).

## <a name="counting-columns"></a>Comptage des colonnes

Assez logiquement, la propriété **Count** retourne le nombre réel d'objets **Field** compris dans la collection **Fields**. La numérotation des membres d'une collection commençant à zéro, vous devez toujours coder les boucles en commençant par le membre zéro et en terminant par la valeur de la propriété **Count** moins 1. Si vous utilisez Microsoft Visual Basic et souhaitez parcourir les éléments d'une collection sans vérifier la valeur de la propriété **Count**, utilisez la commande **For** **Each...Next**.

Si la propriété **Count** a pour valeur zéro, cela signifie que la collection ne contient aucun objet.

## <a name="getting-to-the-field"></a>Accès à l'objet Field

Comme dans toute collection ADO, la propriété **Item** constitue la propriété par défaut de la collection. Elle retourne l'objet **Field** spécifié par le nom ou l'index qui lui est passé. Par conséquent, les instructions suivantes sont équivalentes pour l'exemple d'objet **Recordset**:

```vb 
 
objField = objRecordset.Fields.Item("ProductID") 
objField = objRecordset.Fields("ProductID") 
objField = objRecordset.Fields.Item(0) 
objField = objRecordset.Fields(0) 
```

Si ces méthodes sont équivalentes, vous vous demandez laquelle choisir. Cela dépend. Le recours à un index pour extraire un objet **Field** d'une collection est plus rapide car cela permet d'accéder directement directement à l'objet **Field**, sans devoir effectuer une recherche de chaîne. En revanche, le nombre d'objets **Fields** de la collection doit être connu et, si l'ordre est modifié, la référence à l'index de l'objet **Field** doit être modifiée en conséquence. Bien que cette méthode soit plus lente, l'utilisation du nom de l'objet **Field** offre davantage de souplesse car elle ne dépend pas de l'ordre des objets **Fields** dans la collection.

## <a name="using-the-refresh-method"></a>Utilisation de la méthode Refresh

Contrairement à ce qui se passe pour d'autres collections ADO, l'utilisation de la méthode **Refresh** de la collection **Fields** n'a pas d'effet visible. Pour récupérer les modifications de la structure de base de données sous-jacente, vous devez utiliser la méthode **Requery** ou, si l'objet **Recordset** ne prend pas en charge les signets, la méthode **MoveFirst**, qui provoquera une nouvelle exécution de la commande auprès du fournisseur.

## <a name="adding-fields-to-a-recordset"></a>Ajout de champs à un jeu d'enregistrements

La méthode **Append** permet d'ajouter des champs à un objet **Recordset**.

Vous pouvez utiliser la méthode **Append** pour créer un objet **Recordset** par programme, sans ouvrir de connexion à une source de données. Une erreur d'exécution se produit si la méthode **Append** est appelée sur la collection **Fields** d'un objet **Recordset** ouvert ou sur un objet **Recordset** dans lequel la propriété **ActiveConnection** est définie. Vous pouvez ajouter des champs à un objet **Recordset** uniquement lorsque celui-ci n'est pas ouvert et n'a pas encore été connecté à une source de données. Notez toutefois que, pour spécifier les valeurs de la collection **Fields** récemment ajoutée, l'objet **Recordset** doit être ouvert.

Les développeurs ont parfois besoin d'un emplacement de stockage temporaire pour certaines données, ou souhaitent que certaines données se comportent comme si elles provenaient d'un serveur, pour participer à la liaison des données dans une interface utilisateur. ADO (en association avec le [Service de curseur Microsoft pour OLE DB](microsoft-cursor-service-for-ole-db-ado-service-component.md)) permet de construire un objet **Recordset** vide en spécifiant les informations de colonnes et en appelant la méthode **Open**. Dans l'exemple suivant, trois nouveaux champs sont ajoutés à un nouvel objet **Recordset**. Par la suite, l'objet **Recordset** est ouvert, deux nouveaux enregistrements sont ajoutés et l'objet **Recordset** est stocké de façon persistante dans un fichier. Pour plus d'informations sur la persistance des objets **Recordset**, consultez le [chapitre 5 : Mise à jour et persistance des données](chapter-5-updating-and-persisting-data.md).)

```vb 
 
 'BeginFabricate 
 Dim objRs As New ADODB.Recordset 
 
 With objRs.Fields 
 .Append "StudentID", adChar, 11, adFldUpdatable 
 .Append "FullName", adVarChar, 50, adFldUpdatable 
 .Append "PhoneNmbr", adVarChar, 20, adFldUpdatable 
 End With 
 
 With objRs 
 .Open 
 
 .AddNew 
 .Fields(0) = "123-45-6789" 
 .Fields(1) = "John Doe" 
 .Fields(2) = "(425) 555-5555" 
 .Update 
 
 .AddNew 
 .Fields(0) = "123-45-6780" 
 .Fields(1) = "Jane Doe" 
 .Fields(2) = "(615) 555-1212" 
 .Update 
 End With 
 
 objRs.Save App.Path & "\FabriTest.adtg", adPersistADTG 
 
 objRs.Close 
 'EndFabricate 
```

L'utilisation de la méthode **Append** de la collection **Fields** diffère selon qu'elle concerne un objet **Recordset** ou un objet **Record**. Pour plus d'informations sur les objets **Record**, consultez le [chapitre 10 : Enregistrements et flux](chapter-10-records-and-streams.md).

