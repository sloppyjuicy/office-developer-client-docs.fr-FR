---
title: GetRows, méthode (ADO)
TOCTitle: GetRows Method (ADO)
ms:assetid: 570e6f1c-c17a-7d9a-c172-387894a3a1f1
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249292(v=office.15)
ms:contentKeyID: 48544963
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: fc82a753adb5e9bd7a5a5d46b6ae8ce284a94375
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25469322"
---
# <a name="getrows-method-ado"></a>GetRows, méthode (ADO)


**S’applique à**: Access 2013 | Office 2013


Récupère plusieurs enregistrements d'un objet [Recordset](recordset-object-ado.md) dans un tableau.

## <a name="syntax"></a>Syntaxe

*tableau* = *jeu d’enregistrements*. GetRows (*lignes*, *Démarrez*, *champs* )

## <a name="return-value"></a>Valeur de retour

Retourne une valeur de type **Variant** qui représente un tableau à deux dimensions.

## <a name="parameters"></a>Paramètres

  - *Lignes*

  - Facultatif. Valeur [GetRowsOptionEnum](getrowsoptionenum.md) qui indique le nombre d'enregistrements à récupérer. La valeur par défaut est **adGetRowsRest**.

  - *Début*

  - Facultatif. Valeur de type **String** ou **Variant** qui correspond au signet de l'enregistrement à partir duquel l'opération **GetRows** doit commencer. Vous pouvez également utiliser une valeur [BookmarkEnum](bookmarkenum.md).

  - *Champs*

  - Facultatif. **Variant** qui représente un seul nom de champ ou position ordinale, ou un tableau de noms de champs ou de positions ordinales. ADO retourne uniquement les données de ces champs.

## <a name="remarks"></a>Notes

Utilisez la méthode **GetRows** pour copier des enregistrements d'un objet **Recordset** dans un tableau à deux dimensions. Le premier indice identifie le champ et le second le numéro d'enregistrement. La variable du *tableau* est automatiquement dimensionnée à la taille correcte lorsque la méthode **GetRows** renvoie les données.

Si vous ne spécifiez pas de valeur pour l’argument *lignes* , la méthode **GetRows** récupère automatiquement tous les enregistrements dans l’objet **Recordset** . Si vous demandez plus d'enregistrements que le nombre disponible, **GetRows** retourne uniquement le nombre d'enregistrements disponibles.

Si l’objet **Recordset** prend en charge les signets, vous pouvez spécifier à quel enregistrement la méthode **GetRows** doit commencer à extraire des données en passant la valeur de la propriété [Bookmark](bookmark-property-ado.md) de cet enregistrement dans l’argument *début* .

Si vous souhaitez restreindre les champs de l’appel de **GetRows** , vous pouvez passer un seul nom/numéro ou un tableau de noms/numéros de champ dans l’argument *champs* .

Après avoir appelé **GetRows**, l'enregistrement suivant non lu devient l'enregistrement actif ou, s'il n'y a plus aucun enregistrement, la propriété [EOF](bof-eof-properties-ado.md) a la valeur **True**.

