---
title: TableDef.DateCreated, propriété (DAO)
TOCTitle: DateCreated Property
ms:assetid: fedd28e9-41a4-db7f-9ba9-6ada350d594a
ms:mtpsurl: https://msdn.microsoft.com/library/Ff837292(v=office.15)
ms:contentKeyID: 48548947
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: a5dc326b271e8444211bba0cd2d3c37c047ac205
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32314538"
---
# <a name="tabledefdatecreated-property-dao"></a>TableDef.DateCreated, propriété (DAO)


**S’applique à** : Access 2013, Office 2013

Renvoie la date et l'heure auxquelles un objet a été créé (espaces de travail Microsoft Access uniquement). Type **Variant** en lecture seule.

## <a name="syntax"></a>Syntaxe

*.* DateCreated

*expression* Variable représentant un objet **TableDef**.

## <a name="remarks"></a>Remarques

**DateCreated** et **LastUpdated** renvoient la date et l'heure auxquelles l'objet a été créé ou mis à jour en dernier lieu. Dans un environnement multi-utilisateur, les utilisateurs doivent obtenir ces paramètres directement du serveur de fichiers afin d'éviter des incohérences entre les paramètres des propriétés DateCreated et LastUpdated.

