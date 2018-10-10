---
title: Connection Object (DAO)
TOCTitle: Connection Object
ms:assetid: f469b04e-2539-6b53-31f2-85fe22fcc2fc
ms:mtpsurl: https://msdn.microsoft.com/library/Ff836694(v=office.15)
ms:contentKeyID: 48548690
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: bba06d593069051d2cc4f2e66b8cb91f36d920fb
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25469887"
---
# <a name="connection-object-dao"></a>Connection Object (DAO)


**S’applique à**: Access 2013 | Office 2013


> [!NOTE]
> <P>[!REMARQUE] Les espaces de travail ODBCDirect ne sont pas pris en charge dans Microsoft Access 2013. Utilisez ADO si vous voulez accéder aux sources de données externes sans avoir recours au moteur de base de données Microsoft Access.</P>



Un objet **Connection** représente une connexion à une base de données ODBC (espaces de travail ODBCDirect uniquement).

## <a name="remarks"></a>Remarques

Un objet **Connection** est un objet non persistant, qui représente une connexion à une base de données distante. L'objet **Connection** n'est disponible que dans les espaces de travail ODBCDirect (c'est-à-dire un objet **Workspace** créé avec l'option de type définie sur **dbUseODBC**).


> [!NOTE]
> <P>[!REMARQUE] Le code écrit pour des versions antérieures de DAO peut continuer à utiliser l'objet <STRONG>Database</STRONG> pour la rétrocompatibilité, mais si les nouvelles caractéristiques d'un objet <STRONG>Connection</STRONG> sont souhaitées, vous devez réviser le code de manière à utiliser l'objet <STRONG>Connection</STRONG>. Pour vous aider avec la conversion du code, vous pouvez obtenir une référence d'objet <STRONG>Connection</STRONG> à partir d'un objet <STRONG>Database</STRONG> en lisant la propriété <A href="database-connection-property-dao.md">Connection</A> de l'objet <STRONG>Database</STRONG>. À l'inverse, vous pouvez obtenir une référence d'objet <STRONG>Database</STRONG> à partir de la propriété <STRONG>Database</STRONG> de l'objet <STRONG>Connection</STRONG>.</P>


