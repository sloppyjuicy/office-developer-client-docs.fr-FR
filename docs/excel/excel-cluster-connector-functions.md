---
title: Fonctions du connecteur de Cluster Excel
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 65927ef9-29f7-499a-a1c1-6f672c09bb6b
description: 'S�applique �: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: 4a069aa4ed3ee17320ac65ab793ea8812153cc18
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19782046"
---
# <a name="excel-cluster-connector-functions"></a>Fonctions du connecteur de Cluster Excel

 **S’applique à**: Excel 2013 | Office 2013 | Visual Studio 
  
Connecteur de cluster Microsoft Excel 2013 DLL doit implémenter les fonctions décrites dans cette section.
  
Les valeurs de retour mentionnés dans les rubriques de cette section sont définies dans le SDK de référence incluent le fichier xlcall.h.
  
## <a name="cluster-connector-architecture"></a>Architecture du connecteur de cluster

Excel appelle les points d’entrée dans un connecteur de cluster pour transférer des appels de fonction définie par l’utilisateur à un cluster de calcul hautes performances et de gestion des sessions de cluster.
  
## <a name="in-this-section"></a>Dans cette section

[CallUDF](calludf.md)
  
[CancelOutstandingRequests](canceloutstandingrequests.md)
  
[Méthode CloseSession](closesession.md)
  
[Méthode OpenSession](opensession.md)
  
[PingSession](pingsession.md)
  
[ShowOptions](showoptions.md)
  
## <a name="see-also"></a>Voir aussi



[D�veloppement de connecteurs de Cluster Excel 2013](developing-excel-cluster-connectors.md)
  
[Fonctions sécurisées pour le cluster](cluster-safe-functions.md)

