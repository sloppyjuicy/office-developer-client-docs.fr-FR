---
title: ChildCount, propriété (ADO MD)
TOCTitle: ChildCount property (ADO MD)
ms:assetid: ff1872f0-d5f6-174e-0473-7997a462ca81
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250309(v=office.15)
ms:contentKeyID: 48548956
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 0e52bd6cb6296fa8409658892f68d2ab2aefeda4
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59618524"
---
# <a name="childcount-property-ado-md"></a>ChildCount, propriété (ADO MD)


**S’applique à** : Access 2013, Office 2013

Indique le nombre de membres dont l'objet [Member](member-object-ado-md.md) actif est le parent dans une hiérarchie.

## <a name="return-values"></a>Valeurs de retour

Retourne un entier de type **Long** et est en lecture seule.

## <a name="remarks"></a>Remarques

Utilisez la propriété **ChildCount** pour retourner une estimation du nombre d'enfants d'un objet **Member**. La propriété **Children** peut renvoyer le nombre réel d'enfants d'un objet [Member](children-property-ado-md.md).

Pour les objets **Member** d'un objet [Position](position-object-ado-md.md), le nombre maximum renvoyé est 65 536. Si le nombre réel d'enfants dépasse 65 536, la valeur de retour sera toujours 65 536. L'application doit normalement interpréter une propriété **ChildCount** d'une valeur de 65 536 comme égale ou supérieure à 65 536 enfants.

Pour les objets **Member** d'un objet [Level](level-object-ado-md.md), utilisez la propriété [Count](count-property-ado.md) de la collection ADO sur la collection **Children** afin de déterminer le nombre exact d'enfants. Ce calcul peut prendre du temps si la collection contient un grand nombre d'enfants.

