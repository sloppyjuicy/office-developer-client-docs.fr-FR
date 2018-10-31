---
title: DBEngine.DefaultType Property (DAO)
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
ms.openlocfilehash: ef2c8a4844d02c55db6cea80e0767b4b7f75d114
ms.sourcegitcommit: 801b1b54786f7b0e5b0d35466e7ae8d1e840b26f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25861447"
---
# <a name="dbenginedefaulttype-property-dao"></a>DBEngine.DefaultType Property (DAO)


**S’applique à**: Access 2013 | Office 2013

Définit ou renvoie une valeur qui indique le type d'espace de travail qui sera utilisé par le prochain objet **[Workspace](workspace-object-dao.md)** créé.

## <a name="syntax"></a>Syntaxe

*expression* . DefaultType

*expression* Variable qui représente un objet **DBEngine** .

## <a name="remarks"></a>Remarques

Le paramètre ou la valeur renvoyée peut correspondre à l'une des constantes **[WorkspaceTypeEnum](workspacetypeenum-enumeration-dao.md)**.


> [!NOTE]
> [!REMARQUE] Les espaces de travail ODBCDirect ne sont pas pris en charge dans Microsoft Access 2013. Utilisez ADO si vous voulez accéder aux sources de données externes sans avoir recours au moteur de base de données Microsoft Access.

Le paramètre peut être remplacé pour un objet **Workspace** en définissant l’argument de type à la méthode **[CreateWorkspace](dbengine-createworkspace-method-dao.md)** .

