---
title: Connection, objet (DAO)
TOCTitle: Connection Object
ms:assetid: f469b04e-2539-6b53-31f2-85fe22fcc2fc
ms:mtpsurl: https://msdn.microsoft.com/library/Ff836694(v=office.15)
ms:contentKeyID: 48548690
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: ddc4e580d217d35973fa7a96ad1ed7480fc5aa91
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59627001"
---
# <a name="connection-object-dao"></a>Connection, objet (DAO)

**S’applique à** : Access 2013, Office 2013

> [!NOTE]
> Les espaces de travail ODBCDirect ne sont pas pris en charge dans Microsoft Access 2013. Utilisez ADO si vous voulez accéder aux sources de données externes sans utiliser le moteur de base de données Microsoft Access.

Un objet **Connection** représente une connexion à une base de données ODBC (espaces de travail ODBCDirect uniquement).

## <a name="remarks"></a>Remarques

Un objet **Connection** est un objet non persistant, qui représente une connexion à une base de données distante. L'objet **Connection** n'est disponible que dans les espaces de travail ODBCDirect (c'est-à-dire un objet **Workspace** créé avec l'option de type définie sur **dbUseODBC**).

> [!NOTE]
> [!REMARQUE] Le code écrit pour des versions antérieures de DAO peut continuer à utiliser l'objet **Database** pour la rétrocompatibilité, mais si les nouvelles caractéristiques d'un objet **Connection** sont souhaitées, vous devez réviser le code de manière à utiliser l'objet **Connection**. Pour vous aider avec la conversion du code, vous pouvez obtenir une référence d'objet **Connection** à partir d'un objet **Database** en lisant la propriété [Connection](database-connection-property-dao.md) de l'objet **Database**. À l'inverse, vous pouvez obtenir une référence d'objet **Database** à partir de la propriété **Database** de l'objet **Connection**.


