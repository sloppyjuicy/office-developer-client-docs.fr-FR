---
title: Propriété TableDef.DateCreated (DAO)
TOCTitle: DateCreated Property
ms:assetid: fedd28e9-41a4-db7f-9ba9-6ada350d594a
ms:mtpsurl: https://msdn.microsoft.com/library/Ff837292(v=office.15)
ms:contentKeyID: 48548947
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: be76ed7f9d358963ea58776327ddafbb66f9d367
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/02/2018
ms.locfileid: "25923139"
---
# <a name="tabledefdatecreated-property-dao"></a>Propriété TableDef.DateCreated (DAO)


**S’applique à**: Access 2013, Office 2013

Renvoie la date et l'heure auxquelles un objet a été créé (espaces de travail Microsoft Access uniquement). Valeur **Variant** en lecture seule.

## <a name="syntax"></a>Syntaxe

*expression* . DateCreated

*expression* Variable qui représente un objet **TableDef** .

## <a name="remarks"></a>Remarques

**DateCreated** et **LastUpdated** renvoient la date et l'heure auxquelles l'objet a été créé ou mis à jour en dernier lieu. Dans un environnement multi-utilisateur, les utilisateurs doivent obtenir ces paramètres directement du serveur de fichiers afin d'éviter des incohérences entre les paramètres des propriétés DateCreated et LastUpdated.

