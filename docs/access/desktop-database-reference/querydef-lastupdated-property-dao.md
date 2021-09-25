---
title: Propriété QueryDef.LastUpdated (DAO)
TOCTitle: LastUpdated Property
ms:assetid: 3b7818d4-054e-54e2-bf63-58b340bb4a90
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192665(v=office.15)
ms:contentKeyID: 48544287
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 9938f8ff4aa6625508bdc55115f35fcff5a3e66b
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59617768"
---
# <a name="querydeflastupdated-property-dao"></a>Propriété QueryDef.LastUpdated (DAO)


**S’applique à** : Access 2013, Office 2013

Renvoie la date et l'heure de la dernière modification apportée à un objet. Type de données **Variant** en lecture seule.

## <a name="syntax"></a>Syntaxe

*.* LastUpdated

*expression* Variable représentant un objet **QueryDef**.

## <a name="remarks"></a>Remarques

**DateCreated** et **LastUpdated** renvoient la date et l'heure auxquelles l'objet a été créé ou mis à jour en dernier lieu. Dans un environnement multi-utilisateur, les utilisateurs doivent obtenir ces paramètres directement du serveur de fichiers afin d'éviter des incohérences entre les paramètres des propriétés DateCreated et LastUpdated.

