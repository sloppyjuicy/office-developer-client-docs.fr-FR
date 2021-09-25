---
title: Excel Fonctions du connecteur de cluster
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.localizationpriority: medium
ms.assetid: 65927ef9-29f7-499a-a1c1-6f672c09bb6b
description: 'S’applique à : Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: db4dec310a9c100ffba886b89c4cd82f519aa48a
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59552261"
---
# <a name="excel-cluster-connector-functions"></a>Excel Fonctions du connecteur de cluster

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

