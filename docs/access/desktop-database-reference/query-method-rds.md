---
title: Query, méthode (RDS - référence du bureau de la base de données Access)
TOCTitle: Query method (RDS)
ms:assetid: c88d82bd-2139-7f1e-4e5e-9030f3795816
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249975(v=office.15)
ms:contentKeyID: 48547658
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 1e7f9dfc3ce5cb0d757951f13c1078ab44d04760
ms.sourcegitcommit: 980a96cf444882d3d34cecb5faac8f8a7b7c4b57
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/03/2018
ms.locfileid: "25949424"
---
# <a name="query-method-rds"></a>Query, méthode (RDS)

**S’applique à**: Access 2013, Office 2013

Utilise une chaîne de requête SQL valide qui retourne un objet [Recordset](recordset-object-ado.md).

## <a name="syntax"></a>Syntaxe

Définir le*jeu d’enregistrements* = *DataFactory*. Requête (*connexion*, *requête*)

## <a name="parameters"></a>Paramètres

|Paramètre|Description|
|:--------|:----------|
|*Recordset* |Une variable objet qui représente un objet **Recordset**|
|*DataFactory* |Variable objet représentant un objet [RDSServer.DataFactory](datafactory-object-rdsserver.md).|
|*Connexion* |Valeur de type **String** qui contient les informations de connexion de serveur. Ce paramètre est similaire à la propriété [Connect](connect-property-rds.md).|
|*Requête* |Valeur de type **String** qui contient la requête SQL.|

## <a name="remarks"></a>Notes

La requête doit utiliser le langage SQL du serveur de base de données. Un état de résultat est retourné en cas d'erreur liée à la requête exécutée. La méthode **Query** ne procède à aucun vérification syntaxique de la chaîne du paramètre **Requête**.

