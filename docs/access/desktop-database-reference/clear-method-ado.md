---
title: Méthode Clear - ActiveX Data Objects (ADO)
TOCTitle: Clear method (ADO)
ms:assetid: 5d51f42c-147b-1fcf-d05b-123e5714ecb7
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249329(v=office.15)
ms:contentKeyID: 48545110
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 2cb522a0b70517e81f086f544b1b1e366c166087
ms.sourcegitcommit: 558d09fad81f8d80b5ad0edd21934fc09c098f2c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/03/2018
ms.locfileid: "25947398"
---
# <a name="clear-method-ado"></a>Clear, méthode (ADO)


**S’applique à**: Access 2013, Office 2013

Supprime tous les objets **Error** de la collection **Errors**.

## <a name="syntax"></a>Syntaxe

*Erreurs*. Effacer

## <a name="remarks"></a>Notes

Utilisez la méthode **Clear** de la collection [Errors](errors-collection-ado.md) pour supprimer tous les objets [Error](error-object-ado.md) existants de la collection. En cas d'erreur, ADO supprime automatiquement le contenu de la collection **Errors** et la remplit d'objets **Error** liés à la nouvelle erreur.

Certaines propriétés et méthodes retournent des avertissements qui apparaissent en tant qu'objets **Error** dans la collection **Errors** sans pour autant arrêter l'exécution d'un programme. Avant d'appeler les méthodes [Resync](resync-method-ado.md), [UpdateBatch](updatebatch-method-ado.md) ou [CancelBatch](cancelbatch-method-ado.md) sur un objet [Recordset](recordset-object-ado.md) ou la méthode [Open](open-method-ado-connection.md) sur un objet [Connection](connection-object-ado.md) ou encore avant de définir la propriété [Filter](filter-property-ado.md) sur un objet **Recordset**, appelez la méthode **Clear** sur la collection **Errors**. Ainsi, vous pourrez lire la propriété [Count](count-property-ado.md) de la collection **Errors** afin de vérifier les avertissements retournés.

