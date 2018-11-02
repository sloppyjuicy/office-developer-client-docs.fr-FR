---
title: Close, méthode - ActiveX Data Objects (ADO)
TOCTitle: Close method (ADO)
ms:assetid: 26a7cced-ebeb-70be-f5de-96a35711bc37
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249029(v=office.15)
ms:contentKeyID: 48543818
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 3040896c1613e64a41fb839a7ea111cbca547e00
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/02/2018
ms.locfileid: "25923272"
---
# <a name="close-method-ado"></a>Close, méthode (ADO)


**S’applique à**: Access 2013, Office 2013

Ferme un objet ouvert, ainsi que tous les objets qui en dépendent.

## <a name="syntax"></a>Syntaxe

*object*.Close

## <a name="remarks"></a>Notes

Utilisez la méthode **Close** pour fermer un objet [Connection](connection-object-ado.md), [Record](record-object-ado.md), [Recordset](recordset-object-ado.md) ou [Stream](stream-object-ado.md) et libérer ainsi toutes les ressources système associées. La fermeture d'un objet n'entraîne pas sa suppression de la mémoire ; vous pouvez modifier ses paramètres de propriété et le rouvrir ultérieurement. Pour supprimer définitivement un objet de la mémoire, définissez la variable d’objet sur *Nothing* (dans Visual Basic) après la fermeture de l’objet.

**Objet Connection**

Lorsque vous utilisez la méthode **Close** pour fermer un objet **Connection**, tous les objets **Recordset** actifs associés à cette connexion sont également fermés. Si un objet [Command](command-object-ado.md) est associé à l'objet **Connection** que vous fermez, il est conservé, mais il ne sera plus associé à l'objet **Connection**. En d'autres termes, sa propriété [ActiveConnection](activeconnection-property-ado.md) prendra la valeur **Nothing**. Par ailleurs, les paramètres définis par le fournisseur seront supprimés de la collection **Parameters** de l'objet [Command](parameters-collection-ado.md).

Vous pouvez ensuite appeler la méthode [Open](open-method-ado-connection.md) pour rétablir la connexion à la même source de données ou à une source de données différente. Lorsque l'objet **Connection** est fermé, l'appel d'une méthode nécessitant une connexion ouverte à la source de données génère une erreur.

Lorsque vous fermez un objet **Connection** alors que des objets **Recordset** sont ouverts sur la connexion, les modifications en attente dans tous les objets **Recordset** sont annulées. La fermeture explicite d'un objet **Connection** (par un appel de la méthode **Close** ) alors qu'une transaction est en cours génère une erreur. Si un objet **Connection** devient hors de portée lorsqu'une transaction est en cours, ADO restaure automatiquement la transaction.

Objets **Recordset, Record et Stream**

L'utilisation de la méthode **Close** pour fermer un objet **Recordset**, **Record** ou **Stream** libère les données associées, ainsi que tout accès exclusif aux données dont vous disposiez via cet objet spécifique. Vous pouvez appeler ultérieurement la méthode [Open](open-method-ado-recordset.md) pour rouvrir l'objet avec les mêmes attributs ou avec des attributs modifiés.

Lorsqu'un objet **Recordset** est fermé, l'appel d'une méthode nécessitant un curseur actif génère une erreur.

Lorsqu'une modification est en cours en mode de mise à jour immédiate, l'appel de la méthode **Close** génère une erreur ; vous devez appeler, au préalable, la méthode [Update](update-method-ado.md) ou [CancelUpdate](cancelupdate-method-ado.md). Si vous fermez l'objet **Recordset** en mode de mise à jour par lot, toutes les modifications apportées depuis le dernier appel de la méthode [UpdateBatch](updatebatch-method-ado.md) sont perdues.

Si vous utilisez la méthode [Clone](clone-method-ado.md) pour créer des copies d'un objet **Recordset** ouvert, la fermeture de l'objet d'origine ou d'un clone n'affecte pas les autres copies.

