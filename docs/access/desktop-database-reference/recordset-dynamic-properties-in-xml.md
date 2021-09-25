---
title: Propriétés dynamiques du recordset au format XML
TOCTitle: Recordset dynamic properties in XML
ms:assetid: 6ee1f176-9986-4ade-fc97-e3dad8e6bc6b
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249439(v=office.15)
ms:contentKeyID: 48545522
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 6b61504b6c88b1ccf2a7ff91756e821ae7a2f7af
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59617656"
---
# <a name="recordset-dynamic-properties-in-xml"></a>Propriétés dynamiques du recordset au format XML

**S’applique à** : Access 2013, Office 2013

Les propriétés **Recordset** spécifiques au fournisseur (du moteur du curseur client) suivantes sont actuellement conservées au format XML :

- **AutoRecalc**
- **BatchSize**
- **CommandTimeout**
- **IRowsetChange**
- **IRowsetUpdate**
- **Reshape Name**
- **Resync Command**
- **Unique Catalog**
- **Unique Schema**
- **Unique Table**
- **Update Resync**
- **UpdateCriteria**


Ces propriétés sont enregistrées dans la section de schéma en tant qu'attributs de la définition d'élément du **jeu d'enregistrements** en cours de persistance. Ces attributs sont définis dans l'espace de noms du schéma du jeu de lignes et doivent avoir le préfixe « rs: ».

## <a name="see-also"></a>Voir aussi

- [Propriétés dynamiques ADO](ado-dynamic-properties.md)
