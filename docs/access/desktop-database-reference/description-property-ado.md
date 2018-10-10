---
title: Description, propriété (ADO)
TOCTitle: Description Property (ADO)
ms:assetid: 31df5e36-641c-d213-31fc-6244e2983327
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249092(v=office.15)
ms:contentKeyID: 48544064
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 3837d60b58772bbe6b65af6673c4eaa471507e66
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25469855"
---
# <a name="description-property-ado"></a>Description, propriété (ADO)


**S’applique à**: Access 2013 | Office 2013

Décrit un objet [Error](error-object-ado.md).

## <a name="return-value"></a>Valeur de retour

Renvoie une valeur de type **String** qui contient une description de l'erreur.

## <a name="remarks"></a>Notes

Utilisez la propriété **Description** pour obtenir une courte description de l'erreur. Affichez cette propriété pour avertir l'utilisateur d'une erreur que vous ne pouvez pas ou ne souhaitez pas gérer. La chaîne provient d'ADO ou d'un fournisseur.

Les fournisseurs sont chargés de transmettre un texte d'erreur spécifique à ADO. ADO ajoute un objet [Error](error-object-ado.md) à la collection **Errors** pour chaque erreur ou avertissement de fournisseur reçu. Énumérez la collection **Errors** pour identifier les erreurs transmises par le fournisseur.

