---
title: Excel fonctions cluster connector
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.localizationpriority: medium
ms.assetid: 65927ef9-29f7-499a-a1c1-6f672c09bb6b
ms.openlocfilehash: 71c0d891e6ddbd4e3453d94b92ef521ac6e22082
ms.sourcegitcommit: 193df57ebf141020852d2ebc8cf0931edb71574a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/25/2022
ms.locfileid: "62199403"
---
# <a name="excel-cluster-connector-functions"></a>Excel fonctions cluster connector

 **S’applique à**: Excel 2013 | Office 2013 | Visual Studio 
  
Microsoft Excel 2013 DLLs de connecteur de cluster doivent implémenter les fonctions décrites dans cette section.
  
Les valeurs de retour mentionnées dans les rubriques de référence de cette section sont définies dans le SDK incluent le fichier xlcall.h.
  
## <a name="cluster-connector-architecture"></a>Architecture du connecteur de cluster

Excel appelle des points d’entrée dans un connecteur de cluster pour transférer des appels de fonctions définies par l’utilisateur vers un cluster de calcul hautes performances et pour la gestion des sessions de cluster.
  
## <a name="in-this-section"></a>Dans cette section

[CallUDF](calludf.md)
  
[CancelOutstandingRequests](canceloutstandingrequests.md)
  
[CloseSession](closesession.md)
  
[OpenSession](opensession.md)
  
[PingSession](pingsession.md)
  
[ShowOptions](showoptions.md)
  
## <a name="see-also"></a>Voir aussi



[D�veloppement de connecteurs de Cluster Excel 2013](developing-excel-cluster-connectors.md)
  
[Fonctions sécurisées pour le cluster](cluster-safe-functions.md)

