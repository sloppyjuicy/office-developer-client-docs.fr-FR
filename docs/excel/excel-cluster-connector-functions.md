---
title: Fonctions du connecteur de cluster Excel
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 65927ef9-29f7-499a-a1c1-6f672c09bb6b
description: 'S’applique à : Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 41a5cf1ecb7c8f38f4aa5b62a493b3f45c2fe090
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408585"
---
# <a name="excel-cluster-connector-functions"></a>Fonctions du connecteur de cluster Excel

 **S’applique à** : Excel 2013 | Office 2013 | Visual Studio 
  
Les DLL de connecteur de cluster Microsoft Excel 2013 doivent implémenter les fonctions décrites dans cette section.
  
Les valeurs de retour mentionnées dans les rubriques de référence de cette section sont définies dans le SDK incluent le fichier xlcall.h.
  
## <a name="cluster-connector-architecture"></a>Architecture du connecteur de cluster

Excel appelle des points d’entrée dans un connecteur de cluster pour transférer des appels de fonctions définies par l’utilisateur vers un cluster de calcul hautes performances et pour la gestion des sessions de cluster.
  
## <a name="in-this-section"></a>Contenu de cette section

[CallUDF](calludf.md)
  
[CancelOutstandingRequests](canceloutstandingrequests.md)
  
[CloseSession](closesession.md)
  
[OpenSession](opensession.md)
  
[PingSession](pingsession.md)
  
[ShowOptions](showoptions.md)
  
## <a name="see-also"></a>Voir aussi



[D�veloppement de connecteurs de Cluster Excel 2013](developing-excel-cluster-connectors.md)
  
[Fonctions sécurisées pour le cluster](cluster-safe-functions.md)

