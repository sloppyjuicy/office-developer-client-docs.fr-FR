---
title: Sort, propriété (ADO)
TOCTitle: Sort property (ADO)
ms:assetid: f2a39b7f-8b96-cd1a-8248-71f8b867454a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250230(v=office.15)
ms:contentKeyID: 48548652
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: ab12b9b32ac84cdd2b77959a1bdd23e4b868b4e3
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59611496"
---
# <a name="sort-property-ado"></a>Sort, propriété (ADO)


**S’applique à** : Access 2013, Office 2013

Indique un ou plusieurs noms de champs selon lesquels le [Recordset](recordset-object-ado.md) est trié ; indique en outre si les valeurs des champs sont triés en ordre croissant ou décroissant.

## <a name="settings-and-return-values"></a>Paramètres et valeurs de retour

Définit ou renvoie une valeur **String** qui indique les noms des champs du **Recorset** selon lesquels le tri est réalisé. Les noms sont séparés par des virgules et éventuellement suivis d'un espace puis du mot clé **ASC** (si les valeurs du champ sont triées en ordre croissant) ou **DESC** (si les valeurs du champ sont triées en ordre décroissant). Si aucun mot clé n'est spécifié, les valeurs du champ sont par défaut triées en ordre croissant.

## <a name="remarks"></a>Remarques

Cette propriété exige que la propriété [CursorLocation](cursorlocation-property-ado.md) ait la valeur **adUseClient**. Un index temporaire est créé pour chaque champ spécifié dans la propriété **Sort** si aucun index n'existe déjà.

L'opération de tri est d'une grande efficacité parce que les données ne sont pas réorganisées physiquement mais sont simplement lues dans l'ordre spécifié par l'index.

Le fait de donner une chaîne vide comme valeur à la propriété **Sort** réinitialise les lignes dans leur ordre d'origine et supprime les index temporaires. Les index existants ne sont pas supprimés.

Supposons qu’un objet **Recordset** contienne trois champs nommés *firstName*, *middleInitial* et *lastName*. Définissez la propriété **Sort** sur la chaîne « lastName DESC, firstName ASC », qui trie le jeu d’enregistrements par nom de famille dans l’ordre décroit, puis par prénom dans l’ordre croissant.  Le deuxième prénom (middle initial) est ignoré.

Les champs ne peuvent pas être nommés « ASC » ou « DESC » car ces noms génèrent des conflits avec les mots-clés **ASC** et **DESC**. Si le nom d'un champ génère un conflit, donnez-lui un alias en utilisant le mot-clé **AS** dans la requête qui renvoie le **Recordset**.

