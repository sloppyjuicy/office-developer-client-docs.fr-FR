---
title: Open, méthode (ADO MD)
TOCTitle: Open Method (ADO MD)
ms:assetid: 12395ff6-fe07-325a-2b69-007aa0b11ee6
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248894(v=office.15)
ms:contentKeyID: 48543335
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: d9b39fa77700fcd1553738d359b8efd7097c183a
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25870274"
---
# <a name="open-method-ado-md"></a>Open, méthode (ADO MD)


**S’applique à**: Access 2013, Office 2013

Récupère les résultats d'une requête multidimensionnelle et renvoie les résultats dans un ensemble de cellules.

## <a name="syntax"></a>Syntaxe

*Ensemble de cellules*. Ouvrir la*Source*, *ActiveConnection*

## <a name="parameters"></a>Paramètres

  - *Source*

  - Facultatif. Valeur de type **Variant** qui correspond à une requête multidimensionnelle valide, telle que la requête MDX (Multidimensional Expression). L’argument *Source* correspond à la propriété [Source](source-property-ado-md.md) . Pour plus d'informations sur MDX, voir la documentation relative à OLE DB pour OLAP dans le kit de développement logiciel Microsoft Data Access Components SDK.

  - *ActiveConnection*

  - Facultatif. Valeur de type **Variant** qui correspond à une chaîne spécifiant soit un nom de variable objet [Connection](connection-object-ado.md) ADO valide, soit une définition d'une connexion. L’argument *ActiveConnection* spécifie la connexion dans laquelle ouvrir l’objet [Cellset](cellset-object-ado-md.md) . Si vous passez une définition de connexion pour cet argument, ADO ouvre une nouvelle connexion à l'aide des paramètres spécifiés. L’argument *ActiveConnection* correspond à la propriété [ActiveConnection](activeconnection-property-ado-md.md) .

## <a name="remarks"></a>Notes

La méthode **Open** génère une erreur si l'un de ses paramètres est omis et que sa propriété correspondante n'a pas été définie avant la tentative d'ouverture de l'objet **Cellset**.

