---
title: Open, méthode (ADO MD)
TOCTitle: Open method (ADO MD)
ms:assetid: 12395ff6-fe07-325a-2b69-007aa0b11ee6
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248894(v=office.15)
ms:contentKeyID: 48543335
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 98cceed03af8ba939579d1542421b375e0db64a7
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/02/2018
ms.locfileid: "25927530"
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

