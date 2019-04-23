---
title: Persistance de recordsets hiérarchiques
TOCTitle: Persisting hierarchical Recordsets
ms:assetid: 28f48d4a-1c32-7b60-cd65-51fb87c5380e
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249048(v=office.15)
ms:contentKeyID: 48543872
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 1964d207f2b35eaeaf51b409adc12a41eac6438f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32287579"
---
# <a name="persisting-hierarchical-recordsets"></a>Persistance de recordsets hiérarchiques

**S’applique à** : Access 2013, Office 2013

Vous pouvez enregistrer un objet **Recordset** hiérarchique dans un fichier au format ADTG ou XML en appelant la méthode [Save](save-method-ado.md). Toutefois, sachez que l’enregistrement d’objets **Recordset** hiérarchiques au format XML présente deux restrictions : vous ne pouvez pas enregistrer un objet **Recordset** hiérarchisé au format XML s’il contient des mises à jour en attente, de même que vous ne pouvez pas enregistrer un objet **Recordset** hiérarchique paramétré.

Pour plus d'informations sur le fournisseur de mise en forme de données, consultez [Microsoft Data Shaping Service pour OLE DB (fournisseur de services ADO)](microsoft-data-shaping-service-for-ole-db-ado-service-provider.md) (ADO) et le Data Shaping Service pour OLE DB(OLE DB).

