---
title: ActualSize, propriété (ADO)
TOCTitle: ActualSize Property (ADO)
ms:assetid: 020a414d-e6aa-5fb9-9b77-bd9d10124f8a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248787(v=office.15)
ms:contentKeyID: 48542949
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: d0fa7b4f5fe27c25db51338dd1dfd1a68a936364
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25469093"
---
# <a name="actualsize-property-ado"></a>ActualSize, propriété (ADO)

**S’applique à**: Access 2013 | Office 2013

Indique la longueur réelle de la valeur d'un champ.

## <a name="settings-and-return-values"></a>Paramètres et valeurs de retour

Retourne une valeur de type **Long**. Certains fournisseurs permettent parfois que la propriété soit définie afin de réserver de l'espace pour les données d'objets BLOB (Binary Large Object), auquel cas la valeur par défaut est 0.

## <a name="remarks"></a>Notes

Utilisez la propriété **ActualSize** pour retourner la longueur réelle de la valeur d'un objet [Field](field-object-ado.md). Pour tous les champs, la propriété **ActualSize** est en lecture seule. Si ADO ne peut pas déterminer la longueur de la valeur de l'objet **Field**, la propriété **ActualSize** retourne **adUnknown**.

Les propriétés **ActualSize** et [DefinedSize](definedsize-property-ado.md) sont différentes, comme l'illustre l'exemple suivant. Un objet **Field** avec un type déclaré **adVarChar** et une longueur maximale de 50 caractères retourne la valeur 50 pour la propriété **DefinedSize**, mais la valeur de la propriété **ActualSize** renvoyée correspond à la longueur des données stockées dans le champ de l'enregistrement actif. Les objets **Field** avec une valeur **DefinedSize** supérieure à 255 octets sont traités comme des colonnes de longueur variable.

