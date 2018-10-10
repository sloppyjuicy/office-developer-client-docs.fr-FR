---
title: Conservation des jeux d'enregistrements hiérarchiques
TOCTitle: Persisting Hierarchical Recordsets
ms:assetid: 28f48d4a-1c32-7b60-cd65-51fb87c5380e
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249048(v=office.15)
ms:contentKeyID: 48543872
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 36c6c1d99b01918d848dfde06c26ad6851b1db43
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25470890"
---
# <a name="persisting-hierarchical-recordsets"></a>Conservation des jeux d'enregistrements hiérarchiques


**S’applique à**: Access 2013 | Office 2013

Vous pouvez enregistrer un objet **Recordset** hiérarchique dans un fichier au format ADTG ou XML en appelant la méthode [Save](save-method-ado.md). Toutefois, sachez que l’enregistrement d’objets **Recordset** hiérarchiques au format XML présente deux restrictions : vous ne pouvez pas enregistrer un objet **Recordset** hiérarchisé au format XML s’il contient des mises à jour en attente, de même que vous ne pouvez pas enregistrer un objet **Recordset** hiérarchique paramétré.

Pour plus d'informations sur le fournisseur de mise en forme de données, consultez [Microsoft Data Shaping Service pour OLE DB (fournisseur de services ADO)](microsoft-data-shaping-service-for-ole-db-ado-service-provider.md) (ADO) et le Data Shaping Service pour OLE DB(OLE DB).

