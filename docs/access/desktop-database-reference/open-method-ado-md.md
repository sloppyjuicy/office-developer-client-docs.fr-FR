---
title: Open, méthode (ADO MD)
TOCTitle: Open method (ADO MD)
ms:assetid: 12395ff6-fe07-325a-2b69-007aa0b11ee6
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248894(v=office.15)
ms:contentKeyID: 48543335
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: d35b24285bc8b033382319423085bda50cb37473
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59552744"
---
# <a name="open-method-ado-md"></a>Open, méthode (ADO MD)

**S’applique à** : Access 2013, Office 2013

Récupère les résultats d'une requête multidimensionnelle et renvoie les résultats dans un ensemble de cellules.

## <a name="syntax"></a>Syntaxe

*Cellset*. Open *Source,* *ActiveConnection*

## <a name="parameters"></a>Paramètres

|Paramètre|Description|
|:--------|:----------|
|*Source* |Facultatif. Valeur de type **Variant** qui correspond à une requête multidimensionnelle valide, telle que la requête MDX (Multidimensional Expression). L’argument *Source* correspond à la propriété [Source](source-property-ado-md.md). Pour plus d’informations sur MDX, voir la documentation relative à OLE DB pour OLAP dans le kit de développement logiciel Microsoft Data Access Components SDK.|
|*ActiveConnection* |Facultatif. Valeur de type **Variant** qui correspond à une chaîne spécifiant soit un nom de variable objet [Connection](connection-object-ado.md) ADO valide, soit une définition d’une connexion. L’argument *ActiveConnection* spécifie la connexion avec laquelle l’objet [Cellset](cellset-object-ado-md.md) doit être ouvert. Si vous passez une définition de connexion pour cet argument, ADO ouvre une nouvelle connexion à l’aide des paramètres spécifiés. L’argument *ActiveConnection* correspond à la propriété [ActiveConnection](activeconnection-property-ado-md.md).|

## <a name="remarks"></a>Remarques

La méthode **Open** génère une erreur si l'un de ses paramètres est omis et que sa propriété correspondante n'a pas été définie avant la tentative d'ouverture de l'objet **Cellset**.

