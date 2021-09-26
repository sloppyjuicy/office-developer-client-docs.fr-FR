---
title: Recordset.MoveNext, méthode (DAO)
TOCTitle: MoveNext Method
ms:assetid: 0a1315cf-92f8-b8ef-1542-081e8c2d5be0
ms:mtpsurl: https://msdn.microsoft.com/library/Ff845090(v=office.15)
ms:contentKeyID: 48543142
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: high
ms.openlocfilehash: b924399cebc8bd64a1f234bf31c2fde1e50bcf3f
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59606197"
---
# <a name="recordsetmovenext-method-dao"></a>Recordset.MoveNext, méthode (DAO)


**S’applique à** : Access 2013, Office 2013

Passe à l’enregistrement suivant dans un objet **Recordset** spécifié et en fait l’enregistrement actif.

## <a name="syntax"></a>Syntaxe

*expression* .MoveNext

*expression* Variable représentant un objet **Recordset**.

## <a name="remarks"></a>Remarques

La méthode **Move** permet de passer d’un enregistrement à un autre sans appliquer de condition.

Si vous modifiez l’enregistrement actif, utilisez la méthode **Update** pour enregistrer les modifications avant de passer à un autre enregistrement. Si vous passez à un autre enregistrement sans procéder à la mise à jour, vos modifications seront perdues sans avertissement.

Lorsque vous ouvrez un objet **Recordset**, le premier enregistrement est actif et la propriété **BOF** a la valeur **False**. Si l’objet **Recordset** ne contient pas d’enregistrements, la propriété **BOF** a la valeur **True** et aucun enregistrement n’est actif.

Si vous utilisez **MoveNext** lorsque le dernier enregistrement est à jour, la **EOF** propriété est **vrai**, et aucun enregistrement actif. Si vous utilisez **MoveNext** là encore, une erreur se produit, et **EOF** reste **vrai**.

Si le recordset fait référence à un type de table **Recordset** (espaces de travail Microsoft Access uniquement), le mouvement suit l’index actuel. Vous pouvez définir l’index actuel à l’aide de la propriété **Index** . Si vous ne définissez pas l’index actuel, l’ordre des enregistrements retournés n’est pas défini.

Vous ne pouvez pas appliquer les méthodes **MoveFirst**, **MoveLast** et **MovePrevious** à un objet **Recordset** de type avant uniquement.

Pour faire avancer ou reculer l’enregistrement actif d’un certain nombre d’enregistrements dans un objet **Recordset**, utilisez la méthode **Move**.

