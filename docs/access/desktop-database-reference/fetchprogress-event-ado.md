---
title: FetchProgress, événement (ADO)
TOCTitle: FetchProgress Event (ADO)
ms:assetid: 09145d9a-ea5e-b41c-6c54-33ec83e642a9
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248828(v=office.15)
ms:contentKeyID: 48543114
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 25d062f4ae7008df787394eeb9253b65d6f5d1c8
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25886192"
---
# <a name="fetchprogress-event-ado"></a>FetchProgress, événement (ADO)


**S’applique à**: Access 2013, Office 2013


L'événement **FetchProgress** est régulièrement appelé pendant une opération asynchrone de longue durée, afin de signaler le nombre de lignes déjà extraites de l'objet [Recordset](recordset-object-ado.md).

## <a name="syntax"></a>Syntaxe

FetchProgress*progression*, *MaxProgress*, *adStatus*, *Connection*

## <a name="parameters"></a>Paramètres

  - *Progress*

  - Valeur de type **Long** indiquant le nombre d'enregistrements déjà extraits par l'opération d'extraction.

  - *MaxProgress*

  - Valeur de type **Long** indiquant le nombre maximal prévu d'enregistrements à récupérer.

  - *adStatus*

  - Valeur d'état [EventStatusEnum](eventstatusenum.md).

  - *Connection*

  - Objet **Recordset** représentant le jeu duquel les enregistrements sont extraits.

## <a name="remarks"></a>Notes

Lorsque vous utilisez **FetchProgress** avec un **objet Recordset**enfant, n’oubliez pas que les valeurs des paramètres *Progress* et *MaxProgress* sont dérivées de l’ensemble de lignes [Service de curseur](microsoft-cursor-service-for-ole-db-ado-service-component.md) sous-jacent. Les valeurs retournées représentent le nombre total d'enregistrements de l'ensemble de lignes sous-jacent et pas seulement ceux du chapitre actif.


> [!NOTE]
> [!REMARQUE] Microsoft Visual Basic 6.0 ou ultérieur est requis pour pouvoir utiliser l'événement **FetchProgress** avec Microsoft Visual Basic.


