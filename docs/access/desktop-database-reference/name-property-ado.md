---
title: Name, propriété (ADO)
TOCTitle: Name property (ADO)
ms:assetid: 4b19bd08-ac3c-86f0-471d-06a37a0d4f89
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249234(v=office.15)
ms:contentKeyID: 48544683
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 42b543481e023e10dd79cd42302a5f5f8c98bf93
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59626273"
---
# <a name="name-property-ado"></a>Name, propriété (ADO)


**S’applique à** : Access 2013, Office 2013

Indique le nom d'un objet.

## <a name="settings-and-return-values"></a>Paramètres et valeurs de retour

Définit ou renvoie une valeur **String** indiquant le nom d'un objet.

## <a name="remarks"></a>Remarques

Utilisez la propriété **Name** pour attribuer un nom ou pour récupérer au nom d'un objet **Command**, **Property**, **Field** ou **Parameter**.

La valeur est accessible en lecture/écriture sur un objet **Command** et lecture seule sur un objet **Property**.

Pour un objet **Field**, **Name** est généralement en lecture seule. Toutefois, pour les objets **Field** récemment ajoutés à la collection [Fields](fields-collection-ado.md) d'un objet [Record](record-object-ado.md), **Name** est exceptionnellement accessible en lecture et en écriture après la définition de la propriété [Value](value-property-ado.md) de l'objet **Field** et une fois que le fournisseur de données a ajouté le nouvel objet **Field** en appelant la méthode [Update](update-method-ado.md) de la collection **Fields**.

Pour les objets **Parameter** qui n'ont pas encore été ajoutés à la collection [Parameters](parameters-collection-ado.md), la propriété **Name** est accessible en lecture/écriture. Pour les objets **Parameter** ajoutés et tous les autres objets, la propriété **Name** est en lecture seule. Les noms peuvent exister en double au sein de la même collection.

Vous pouvez retrouver la propriété **Nom** d'un objet par une référence ordinale, après laquelle il est possible de référencer directement le nom de l'objet. Par exemple, si rstMain.Properties(20). Le nom produit updatability , vous pouvez par la suite faire référence à cette propriété comme produit Updatability , vous pouvez ensuite faire référence à cette propriété en tant que rstMain.Properties(« Updatability ») .

