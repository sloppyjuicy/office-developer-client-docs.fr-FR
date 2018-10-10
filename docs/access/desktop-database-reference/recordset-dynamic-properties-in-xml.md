---
title: Propriétés dynamiques du jeu d'enregistrements au format XML
TOCTitle: Recordset Dynamic Properties in XML
ms:assetid: 6ee1f176-9986-4ade-fc97-e3dad8e6bc6b
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249439(v=office.15)
ms:contentKeyID: 48545522
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 4193220e450c59e7293ed6befa37d8da23801f27
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25469421"
---
# <a name="recordset-dynamic-properties-in-xml"></a>Propriétés dynamiques du jeu d'enregistrements au format XML


**S’applique à**: Access 2013 | Office 2013

## <a name="recordset-dynamic-properties-in-xml"></a>Propriétés dynamiques du jeu d'enregistrements au format XML

Les propriétés **Recordset** spécifiques au fournisseur (du moteur du curseur client) suivantes sont actuellement conservées au format XML :

  - **Update Resync**

  - **Unique Table**

  - **Unique Schema**

  - **Unique Catalog**

  - **Resync Command**

  - **IRowsetChange**

  - **IRowsetUpdate**

  - **CommandTimeout**

  - **BatchSize**

  - **UpdateCriteria**

  - **Reshape Name**

  - **AutoRecalc**

Ces propriétés sont enregistrées dans la section de schéma en tant qu'attributs de la définition d'élément du **jeu d'enregistrements** en cours de persistance. Ces attributs sont définis dans l'espace de noms du schéma du jeu de lignes et doivent avoir le préfixe « rs: ».

