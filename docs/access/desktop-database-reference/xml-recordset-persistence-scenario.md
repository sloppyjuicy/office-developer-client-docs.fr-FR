---
title: Scénario de persistance des objets Recordset XML
TOCTitle: XML Recordset Persistence Scenario
ms:assetid: 08f464da-10ba-b649-7571-766a40da2e04
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248825(v=office.15)
ms:contentKeyID: 48543107
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 378d3b1fc559cc07c1eb3a58621a8a4bd09a06ab
ms.sourcegitcommit: 801b1b54786f7b0e5b0d35466e7ae8d1e840b26f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25861823"
---
# <a name="xml-recordset-persistence-scenario"></a>Scénario de persistance du recordset au format XML

**S’applique à**: Access 2013 | Office 2013

## <a name="xml-recordset-persistence-scenario"></a>Scénario de persistance du recordset au format XML

Ce scénario consiste à créer une application ASP (Active Server Pages) enregistrant directement le contenu d'un objet **Recordset** dans l'objet **Response** ASP.

> [!NOTE]
> [!REMARQUE] Pour les besoins de ce scénario, Internet Information Server 5.0 (IIS) ou une version ultérieure doit être installé sur votre serveur.

L'objet **Recordset** retourné est affiché dans Internet Explorer à l'aide d'un objet [RDS.DataControl](datacontrol-object-rds.md).

Pour créer ce scénario, il est nécessaire d'exécuter les étapes suivantes :

1.  Configurer l'application

2.  Obtenir les données

3.  Envoyer les données

4.  Recevoir et afficher les données

### <a name="next-step"></a>Étape suivante

[Étape 1 : configurer l'application](step-1-set-up-the-application.md)

