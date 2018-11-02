---
title: Méthode Recordset2.MoveNext (DAO)
TOCTitle: MoveNext Method
ms:assetid: 0eeb917e-f76a-03ec-9e1e-aa8d501db031
ms:mtpsurl: https://msdn.microsoft.com/library/Ff845265(v=office.15)
ms:contentKeyID: 48543254
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: e89a82a1449fd1a16e5273531a542332542ecdcd
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/02/2018
ms.locfileid: "25923713"
---
# <a name="recordset2movenext-method-dao"></a>Méthode Recordset2.MoveNext (DAO)


**S’applique à**: Access 2013, Office 2013

Se déplace jusqu'à l'enregistrement suivant dans un objet **Recordset** spécifié et définit cet enregistrement comme l'enregistrement actif.

## <a name="syntax"></a>Syntaxe

*expression* . MoveNext

*expression* Variable qui représente un objet **Recordset2** .

## <a name="remarks"></a>Remarques

Utilisez les méthodes **Move** pour vous déplacer entre les enregistrements sans appliquer de condition.

Si vous modifiez l'enregistrement actif, veillez à utiliser la méthode **Update** pour enregistrer les modifications avant de passer à un autre enregistrement. Si vous accédez à un autre enregistrement alors que vous effectuez une mise à jour, les modifications seront perdues sans notification.

Lorsque vous ouvrez un objet **Recordset**, le premier enregistrement est actif et la propriété **BOF** prend la valeur **False**. Si l'objet **Recordset** ne contient pas d'enregistrement, la propriété **BOF** prend la valeur **True**, et il n'y a pas d'enregistrement actif.

Si vous utilisez **MoveNext** lorsque le dernier enregistrement est l'enregistrement actif, la propriété **EOF** prend la valeur **True**, et il n'y a pas d'enregistrement actif. Si vous utilisez de nouveau **MoveNext**, une erreur se produit et **EOF** conserve la valeur **True**.

Si le jeu d’enregistrements fait référence à un **objet Recordset** de type table (espaces de travail Microsoft Access uniquement), le déplacement suit l’index actuel. Vous pouvez définir l'index actif à l'aide de la propriété **Index**. Si vous ne définissez pas l'index actif, l'ordre des enregistrements renvoyés est indéfini.

Vous ne pouvez pas utiliser les méthodes **MoveFirst**, **MoveLast**et **MovePrevious** sur un objet **Recordset** de type avant uniquement.

Pour déplacer la position de l'enregistrement actif dans un objet **Recordset** d'un objet d'un nombre d'enregistrements spécifique vers l'avant ou l'arrière, utilisez la méthode **Move**.

