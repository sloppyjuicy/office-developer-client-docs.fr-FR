---
title: Objet Connection (DAO)
TOCTitle: Connection Object
ms:assetid: f469b04e-2539-6b53-31f2-85fe22fcc2fc
ms:mtpsurl: https://msdn.microsoft.com/library/Ff836694(v=office.15)
ms:contentKeyID: 48548690
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 0473a3f4b920e05ad07556b070ed0e778d7ac694
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/02/2018
ms.locfileid: "25930153"
---
# <a name="connection-object-dao"></a>Objet Connection (DAO)


**S’applique à**: Access 2013, Office 2013

> [!NOTE]
> [!REMARQUE] Les espaces de travail ODBCDirect ne sont pas pris en charge dans Microsoft Access 2013. Utilisez ADO si vous voulez accéder aux sources de données externes sans avoir recours au moteur de base de données Microsoft Access.



Un objet **Connection** représente une connexion à une base de données ODBC (espaces de travail ODBCDirect uniquement).

## <a name="remarks"></a>Remarques

Un objet **Connection** est un objet non persistant, qui représente une connexion à une base de données distante. L'objet **Connection** n'est disponible que dans les espaces de travail ODBCDirect (c'est-à-dire un objet **Workspace** créé avec l'option de type définie sur **dbUseODBC**).


> [!NOTE]
> [!REMARQUE] Le code écrit pour des versions antérieures de DAO peut continuer à utiliser l'objet **Database** pour la rétrocompatibilité, mais si les nouvelles caractéristiques d'un objet **Connection** sont souhaitées, vous devez réviser le code de manière à utiliser l'objet **Connection**. Pour vous aider avec la conversion du code, vous pouvez obtenir une référence d'objet **Connection** à partir d'un objet **Database** en lisant la propriété [Connection](database-connection-property-dao.md) de l'objet **Database**. À l'inverse, vous pouvez obtenir une référence d'objet **Database** à partir de la propriété **Database** de l'objet **Connection**.


