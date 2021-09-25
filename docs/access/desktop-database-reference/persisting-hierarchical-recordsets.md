---
title: Persistance de recordsets hiérarchiques
TOCTitle: Persisting hierarchical Recordsets
ms:assetid: 28f48d4a-1c32-7b60-cd65-51fb87c5380e
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249048(v=office.15)
ms:contentKeyID: 48543872
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: fc89707d2eba81b4045eab93effc63ea71b9af58
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59626206"
---
# <a name="persisting-hierarchical-recordsets"></a>Persistance de recordsets hiérarchiques

**S’applique à** : Access 2013, Office 2013

Vous pouvez enregistrer un objet **Recordset** hiérarchique dans un fichier au format ADTG ou XML en appelant la méthode [Save](save-method-ado.md). Toutefois, sachez que l’enregistrement d’objets **Recordset** hiérarchiques au format XML présente deux restrictions : vous ne pouvez pas enregistrer un objet **Recordset** hiérarchisé au format XML s’il contient des mises à jour en attente, de même que vous ne pouvez pas enregistrer un objet **Recordset** hiérarchique paramétré.

Pour plus d'informations sur le fournisseur de mise en forme de données, consultez [Microsoft Data Shaping Service pour OLE DB (fournisseur de services ADO)](microsoft-data-shaping-service-for-ole-db-ado-service-provider.md) (ADO) et le Data Shaping Service pour OLE DB(OLE DB).

