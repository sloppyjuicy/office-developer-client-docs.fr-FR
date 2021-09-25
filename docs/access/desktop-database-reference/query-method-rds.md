---
title: Méthode de requête (RDS - Référence de base de données de bureau Access)
TOCTitle: Query method (RDS)
ms:assetid: c88d82bd-2139-7f1e-4e5e-9030f3795816
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249975(v=office.15)
ms:contentKeyID: 48547658
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 965dbe7736483c6e2cc926ec4f9fc037e503089b
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59562425"
---
# <a name="query-method-rds"></a>Query, méthode (RDS)

**S’applique à** : Access 2013, Office 2013

Utilise une chaîne de requête SQL valide qui retourne un objet [Recordset](recordset-object-ado.md).

## <a name="syntax"></a>Syntaxe

Définissez *Recordset*  =  *DataFactory*. Query(*Connection*, *Query*)

## <a name="parameters"></a>Paramètres

|Paramètre|Description|
|:--------|:----------|
|*Recordset* |Une variable objet qui représente un objet **Recordset**|
|*DataFactory* |Variable objet représentant un objet [RDSServer.DataFactory](datafactory-object-rdsserver.md).|
|*Connexion* |Valeur de type **String** qui contient les informations de connexion de serveur. Ce paramètre est similaire à la propriété [Connect](connect-property-rds.md).|
|*Requête* |Valeur de type **String** qui contient la requête SQL.|

## <a name="remarks"></a>Remarques

La requête doit utiliser le langage SQL du serveur de base de données. Un état de résultat est retourné en cas d'erreur liée à la requête exécutée. La méthode **Query** ne procède à aucun vérification syntaxique de la chaîne du paramètre **Requête**.

