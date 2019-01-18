---
title: Propriété DBEngine.DefaultType (DAO)
TOCTitle: DefaultType Property
ms:assetid: b4371f3e-1ce0-1d0f-93a8-0c5329b510ab
ms:mtpsurl: https://msdn.microsoft.com/library/Ff822060(v=office.15)
ms:contentKeyID: 48547217
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1053580
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 23f6c87ede6da2cc5b2f3203bfa13cb17bf93e82
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: fr-FR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28713589"
---
# <a name="dbenginedefaulttype-property-dao"></a>Propriété DBEngine.DefaultType (DAO)


**S’applique à**: Access 2013, Office 2013

Définit ou renvoie une valeur qui indique le type d'espace de travail qui sera utilisé par le prochain objet **[Workspace](workspace-object-dao.md)** créé.

## <a name="syntax"></a>Syntaxe

*expression* . DefaultType

*expression* Variable qui représente un objet **DBEngine** .

## <a name="remarks"></a>Remarques

Le paramètre ou la valeur renvoyée peut correspondre à l'une des constantes **[WorkspaceTypeEnum](workspacetypeenum-enumeration-dao.md)**.


> [!NOTE]
> [!REMARQUE] Les espaces de travail ODBCDirect ne sont pas pris en charge dans Microsoft Access 2013. Utilisez ADO si vous voulez accéder aux sources de données externes sans avoir recours au moteur de base de données Microsoft Access.

Le paramètre peut être remplacé pour un objet **Workspace** en définissant l’argument de type à la méthode **[CreateWorkspace](dbengine-createworkspace-method-dao.md)** .

