---
title: Size, propriété (ADO)
TOCTitle: Size property (ADO)
ms:assetid: 24596b5c-b1cc-e97e-68b6-8ff53baf150b
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249017(v=office.15)
ms:contentKeyID: 48543753
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 2a1bed3454d081b9d5de3a01e9b326130b40baa4
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: fr-FR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28711608"
---
# <a name="size-property-ado"></a>Size, propriété (ADO)


**S’applique à**: Access 2013, Office 2013

Indique la taille maximale, en octets ou en caractères, d'un objet [Parameter](parameter-object-ado.md).

## <a name="settings-and-return-values"></a>Paramètres et valeurs de retour

Définit ou retourne une valeur de type **Long** qui indique la taille maximale, en octets ou en caractères, d'une valeur dans un objet **Parameter**.

## <a name="remarks"></a>Remarques

Utilisez la propriété **Size** pour déterminer la taille maximale des valeurs devant être écrites ou lues dans la propriété [Value](value-property-ado.md) d'un objet **Parameter**.

Si vous spécifiez un type de données de longueur variable pour un objet **Parameter** (par exemple tout type de **String**, comme **adVarChar**), vous devez définir la propriété **Size** de l’objet avant de l’ajouter à la collection [Parameters](parameters-collection-ado.md) ; sinon, une erreur est générée.

Si vous avez déjà ajouté l'objet **Parameter** à la collection **Parameters** d'un objet [Command](command-object-ado.md) et que modifiez son type pour un type de données de longueur variable, vous devez définir la propriété **Size** de l'objet **Parameter** avant d'exécuter l'objet **Command**; sinon, une erreur est générée.

Si vous utilisez la méthode [Refresh](refresh-method-ado.md) pour obtenir du fournisseur des informations sur les paramètres et qu'il renvoie des objets **Parameter** contenant un ou plusieurs types de données de longueur variable, il se peut qu'ADO alloue de la mémoire aux paramètres en fonction de leur taille potentielle maximale, ce qui risque de générer une erreur à l'exécution. Pour éviter les erreurs, définissez explicitement la propriété **Size** de ces paramètres avant d'exécuter la commande.

La propriété **Size** est en accessible lecture et en écriture.

