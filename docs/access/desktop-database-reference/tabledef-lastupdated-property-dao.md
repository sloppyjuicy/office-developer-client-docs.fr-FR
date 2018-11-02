---
title: Propriété TableDef.LastUpdated (DAO)
TOCTitle: LastUpdated Property
ms:assetid: fafe54e2-2cf0-5874-92b9-6e20a65e77ef
ms:mtpsurl: https://msdn.microsoft.com/library/Ff837164(v=office.15)
ms:contentKeyID: 48548859
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 81d8dfd040ef7df954b71f724ed1d2689d5d4b33
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/02/2018
ms.locfileid: "25928221"
---
# <a name="tabledeflastupdated-property-dao"></a>Propriété TableDef.LastUpdated (DAO)


**S’applique à**: Access 2013, Office 2013

Renvoie la date et l'heure de la dernière modification apportée à un objet. Type de données **Variant** en lecture seule.

## <a name="syntax"></a>Syntaxe

*expression* . LastUpdated

*expression* Variable qui représente un objet **TableDef** .

## <a name="remarks"></a>Remarques

**DateCreated** et **LastUpdated** renvoient la date et l'heure auxquelles l'objet a été créé ou mis à jour en dernier lieu. Dans un environnement multi-utilisateur, les utilisateurs doivent obtenir ces paramètres directement du serveur de fichiers afin d'éviter des incohérences entre les paramètres des propriétés DateCreated et LastUpdated.

