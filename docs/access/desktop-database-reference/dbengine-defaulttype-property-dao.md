---
title: DBEngine.DefaultType, propriété (DAO)
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
ms.localizationpriority: medium
ms.openlocfilehash: 619d46e493f45745d47a9bb8188df8dfe240c3ba
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59632076"
---
# <a name="dbenginedefaulttype-property-dao"></a>DBEngine.DefaultType, propriété (DAO)


**S’applique à** : Access 2013, Office 2013

Définit ou renvoie une valeur qui indique le type d'espace de travail qui sera utilisé par le prochain objet **[Workspace](workspace-object-dao.md)** créé.

## <a name="syntax"></a>Syntaxe

*.* DefaultType

*expression* Variable représentant un objet **DBEngine**.

## <a name="remarks"></a>Remarques

Le paramètre ou la valeur renvoyée peut correspondre à l'une des constantes **[WorkspaceTypeEnum](workspacetypeenum-enumeration-dao.md)**.


> [!NOTE]
> Les espaces de travail ODBCDirect ne sont pas pris en charge dans Microsoft Access 2013. Utilisez ADO si vous voulez accéder aux sources de données externes sans utiliser le moteur de base de données Microsoft Access.

Le paramètre peut être retravaillé pour un seul espace de travail en attériant l’argument type sur **[la méthode CreateWorkspace.](dbengine-createworkspace-method-dao.md)** 

