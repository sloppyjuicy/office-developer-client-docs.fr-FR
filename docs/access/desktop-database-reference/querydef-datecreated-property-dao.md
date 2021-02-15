---
title: QueryDef.DateCreated, propriété (DAO)
TOCTitle: DateCreated Property
ms:assetid: f7585b34-8314-fb9f-daa6-cd1a8ad59d91
ms:mtpsurl: https://msdn.microsoft.com/library/Ff836910(v=office.15)
ms:contentKeyID: 48548763
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: a4a120eed6c20db73e1c23f31ea9329d00da2f0d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32301070"
---
# <a name="querydefdatecreated-property-dao"></a>QueryDef.DateCreated, propriété (DAO)


**S’applique à** : Access 2013, Office 2013

Renvoie la date et l'heure auxquelles un objet a été créé (espaces de travail Microsoft Access uniquement). Type **Variant** en lecture seule.

## <a name="syntax"></a>Syntaxe

*.* DateCreated

*expression* Variable représentant un objet **QueryDef**.

## <a name="remarks"></a>Remarques

**DateCreated** et **LastUpdated** renvoient la date et l'heure auxquelles l'objet a été créé ou mis à jour en dernier lieu. Dans un environnement multi-utilisateur, les utilisateurs doivent obtenir ces paramètres directement du serveur de fichiers afin d'éviter des incohérences entre les paramètres des propriétés DateCreated et LastUpdated.

