---
title: Propriété QueryDef.LastUpdated (DAO)
TOCTitle: LastUpdated Property
ms:assetid: 3b7818d4-054e-54e2-bf63-58b340bb4a90
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192665(v=office.15)
ms:contentKeyID: 48544287
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 98bb600e6f3f1c9587eca110269e8b6b3765e40f
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/02/2018
ms.locfileid: "25921270"
---
# <a name="querydeflastupdated-property-dao"></a>Propriété QueryDef.LastUpdated (DAO)


**S’applique à**: Access 2013, Office 2013

Renvoie la date et l'heure de la dernière modification apportée à un objet. Type de données **Variant** en lecture seule.

## <a name="syntax"></a>Syntaxe

*expression* . LastUpdated

*expression* Variable qui représente un objet **QueryDef** .

## <a name="remarks"></a>Remarques

**DateCreated** et **LastUpdated** renvoient la date et l'heure auxquelles l'objet a été créé ou mis à jour en dernier lieu. Dans un environnement multi-utilisateur, les utilisateurs doivent obtenir ces paramètres directement du serveur de fichiers afin d'éviter des incohérences entre les paramètres des propriétés DateCreated et LastUpdated.

