---
title: AppendChunk, méthode (ADO)
TOCTitle: AppendChunk method (ADO)
ms:assetid: 3fa931a3-2cd7-a3b0-a750-40e18bc9937e
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249179(v=office.15)
ms:contentKeyID: 48544405
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 9103135100c5a10931ee63bfbdeabe9d97119fd2
ms.sourcegitcommit: 980a96cf444882d3d34cecb5faac8f8a7b7c4b57
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/03/2018
ms.locfileid: "25949263"
---
# <a name="appendchunk-method-ado"></a>AppendChunk, méthode (ADO)

**S’applique à**: Access 2013, Office 2013

Cette méthode ajoute des données à un objet [Field](field-object-ado.md) de données binaires ou de texte volumineux ou à un objet [Parameter](parameter-object-ado.md).

## <a name="syntax"></a>Syntaxe

*objet.* AppendChunk *données*

## <a name="parameters"></a>Paramètres

|Paramètre|Description|
|:--------|:----------|
|*object* |Objet **Field** ou **Parameter**.|
|*Data* |**Variant** contenant les données à ajouter à l'objet.|

## <a name="remarks"></a>Notes

Utilisez la méthode **AppendChunk** sur un objet **Field** ou **Parameter** à remplir avec des données binaires longues ou caractères. Si vous manquez de mémoire système, vous pouvez utiliser la méthode **AppendChunk** pour manipuler une partie des valeurs longues plutôt que leur totalité.

**Champ**

Si le bit **adFldLong** de la propriété [Attributes](attributes-property-ado.md) d'un objet **Field** a la valeur true, vous pouvez appliquer la méthode **AppendChunk** à ce champ.

La première invocation de la méthode **AppendChunk** sur un objet **Field** écrit les données dans le champ en écrasant toute donnée existante. Les invocations suivantes de **AppendChunk** s'ajoutent aux données existantes. Si vous ajoutez des données à un champ, puis définissez ou lisez la valeur d'un autre champ de l'enregistrement actif, ADO suppose que vous avez terminé l'ajout de données dans le premier champ. Si vous invoquez à nouveau la méthode **AppendChunk** sur le premier champ, ADO interprète l'invocation comme une nouvelle opération **AppendChunk** et écrase les données existantes. L'accès à des champs d'autres objets [Recordset](recordset-object-ado.md) non identiques au premier objet **Recordset** n'interrompt pas les opérations **AppendChunk**.

S'il n'existe pas d'enregistrement actif lorsque vous appelez la méthode **AppendChunk** sur un objet **Field**, une erreur se produit.


> [!NOTE]
> [!REMARQUE] La méthode **AppendChunk** ne fonctionne pas sur les objets **Field** d'un objet [Record](record-object-ado.md) ; elle n'exécute aucune opération et génère une erreur d'exécution.



**Paramètre**

Si le bit **adParamLong** de la propriété **Attributes** d'un objet **Parameter** a la valeur true, vous pouvez utiliser la méthode **AppendChunk** pour ce paramètre.

Le premier appel **AppendChunk** sur un objet **Parameter** écrit des données dans ce paramètre en remplaçant les données existantes. Les appels suivants **AppendChunk** sur un objet **Parameter** ajoutent paramètre aux données existantes. Un appel à **AppendChunk** qui passe une valeur null annule toutes les données de paramètre.

