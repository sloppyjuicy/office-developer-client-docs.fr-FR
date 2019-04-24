---
title: Description, propriété (ADO)
TOCTitle: Description property (ADO)
ms:assetid: 31df5e36-641c-d213-31fc-6244e2983327
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249092(v=office.15)
ms:contentKeyID: 48544064
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: ba6d05aa1bfb626520af60a30279983bae6fa566
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32293930"
---
# <a name="description-property-ado"></a>Description, propriété (ADO)


**S’applique à** : Access 2013, Office 2013

Décrit un objet [Error](error-object-ado.md).

## <a name="return-value"></a>Valeur renvoyée

Renvoie une valeur de type **String ** qui contient une description de l'erreur.

## <a name="remarks"></a>Remarques

Utilisez la propriété **Description** pour obtenir une courte description de l'erreur. Affichez cette propriété pour avertir l'utilisateur d'une erreur que vous ne pouvez pas ou ne souhaitez pas gérer. La chaîne provient d'ADO ou d'un fournisseur.

Les fournisseurs sont chargés de transmettre un texte d'erreur spécifique à ADO. ADO ajoute un objet [Error](error-object-ado.md) à la collection **Errors** pour chaque erreur ou avertissement de fournisseur reçu. Énumérez la collection **Errors** pour identifier les erreurs transmises par le fournisseur.

