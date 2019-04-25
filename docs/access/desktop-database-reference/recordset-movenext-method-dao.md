---
title: Recordset.MoveNext, méthode (DAO)
TOCTitle: MoveNext Method
ms:assetid: 0a1315cf-92f8-b8ef-1542-081e8c2d5be0
ms:mtpsurl: https://msdn.microsoft.com/library/Ff845090(v=office.15)
ms:contentKeyID: 48543142
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Priority
ms.openlocfilehash: 1b0ebe0edcfcbfac5942fc83a3ff1f99eddfea7f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32300342"
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

Si recordset fait référence à un objet **Recordset** de type table (espaces de travail Microsoft Access uniquement), le déplacement suit l’index actuel. Vous pouvez définir l’index en cours à l’aide de la **Index** propriété. Si vous ne définissez l’index en cours, l’ordre des enregistrements renvoyés n’est pas défini.

Vous ne pouvez pas appliquer les méthodes **MoveFirst**, **MoveLast** et **MovePrevious** à un objet **Recordset** de type avant uniquement.

Pour faire avancer ou reculer l’enregistrement actif d’un certain nombre d’enregistrements dans un objet **Recordset**, utilisez la méthode **Move**.

