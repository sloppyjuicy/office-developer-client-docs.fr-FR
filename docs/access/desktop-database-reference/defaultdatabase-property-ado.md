---
title: DefaultDatabase, propriété (ADO)
TOCTitle: DefaultDatabase property (ADO)
ms:assetid: a35c5631-f9d9-e51f-950b-e52169830d94
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249757(v=office.15)
ms:contentKeyID: 48546784
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 01ca42ff738afe3a35cab6263cdae32ac256f3d1
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32294147"
---
# <a name="defaultdatabase-property-ado"></a>DefaultDatabase, propriété (ADO)


**S’applique à** : Access 2013, Office 2013

Indique la base de données par défaut d'un objet [Connection](connection-object-ado.md).

## <a name="settings-and-return-values"></a>Paramètres et valeurs de retour

Définit ou renvoie une valeur de type **String**, qui correspond au nom d’une base de données disponible du fournisseur.

## <a name="remarks"></a>Remarques

Utilisez la propriété **DefaultDatabase** pour définir ou retourner le nom de la base de données par défaut d'un objet **Connection** spécifique.

S'il existe une base de données par défaut, les chaînes SQL peuvent utiliser une syntaxe non qualifiée pour accéder aux objets de cette base de données. Pour accéder aux objets dans une base de données autre que celle spécifiée dans la propriété **DefaultDatabase**, vous devez qualifier les noms d'objet avec le nom de la base de données souhaitée. Lors de la connexion, le fournisseur écrit les informations de la base de données par défaut dans la propriété **DefaultDatabase**. Certains fournisseurs n'autorisent qu'une seule base de données par connexion, auquel cas vous ne pouvez pas modifier la propriété **DefaultDatabase**.

Il se peut que certains fournisseurs et sources de données ne prennent pas en charge cette fonctionnalité et retournent une erreur ou une chaîne vide.

**Utilisation des services de données à distance** Cette propriété n'est pas disponible pour un objet **Connection** côté client.

