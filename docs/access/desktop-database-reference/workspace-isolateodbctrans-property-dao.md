---
title: Workspace.IsolateODBCTrans, propriété (DAO)
TOCTitle: IsolateODBCTrans Property
ms:assetid: f7a48358-870b-cad3-d4ef-e46b50428e12
ms:mtpsurl: https://msdn.microsoft.com/library/Ff836924(v=office.15)
ms:contentKeyID: 48548770
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1053083
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 781679dfbd4050cfde219802db4cd9e1544d83ae
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32302512"
---
# <a name="workspaceisolateodbctrans-property-dao"></a>Workspace.IsolateODBCTrans, propriété (DAO)


**S’applique à** : Access 2013, Office 2013

Définit ou renvoie une valeur qui indique si plusieurs transactions impliquant la même source de données ODBC connectée au moteur de base de données Microsoft Access sont isolées (espaces de travail Microsoft Access uniquement).

## <a name="syntax"></a>Syntaxe

*.* IsolateODBCTrans

*expression* Variable qui représente un objet **Workspace**.

## <a name="remarks"></a>Remarques

Dans certaines situations, il est nécessaire d'avoir plusieurs transactions simultanées en cours sur la même connexion ODBC. Pour ce faire, vous devez ouvrir un objet **Workspace** séparé pour chaque transaction. Bien que chaque objet **Workspace** peut avoir sa propre connexion ODBC à la base de données, ceci ralentit les performances du système. Éant donné que l'isolation des transactions est souvent inutile, les connexions ODBC à partir de plusieurs objets **Workspace** ouverts par le même utilisateur sont partagées par défaut.

Certains serveurs ODBC, comme Microsoft SQL Server, n'autorisent pas les transactions simultanées sur une connexion unique. Si vous avez besoin de plusieurs transactions simultanées en cours sur une telle base de données, définissez la propriété **IsolateODBCTrans** sur **True** pour chaque objet **Workspace** dès que vous l'ouvrez. Ce faisant, vous forcez l'ouverture d'une connexion ODBC séparée pour chaque objet **Workspace**.

