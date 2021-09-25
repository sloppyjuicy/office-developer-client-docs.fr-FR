---
title: Affichage des feuilles de propriétés de configuration
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: c9386b98-615f-488c-8212-11d9abebbdcf
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 09283aa35b0f464822edc6b389f91a45ce135193
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59551687"
---
# <a name="displaying-configuration-property-sheets"></a>Affichage des feuilles de propriétés de configuration

**S’applique à** : Outlook 2013 | Outlook 2016 
  
Les fournisseurs de transport utilisent la méthode [IMAPISupport::D oConfigPropsheet](imapisupport-doconfigpropsheet.md) pour implémenter des feuilles de propriétés de configuration. Lors de **l’appel de DoConfigPropSheet,** le fournisseur de transport transmet un pointeur vers un tableau de propriétés, ainsi que des informations sur leur affichage. MAPI présente ensuite les propriétés à l’utilisateur au moyen d’une boîte de dialogue standard. Nous vous encourageons vivement à utiliser ce mécanisme de feuille de propriétés lors de l’implémentation de votre fournisseur de transport en raison de l’avantage pour l’utilisateur d’une interface cohérente.
  
## <a name="transport-providers"></a>Fournisseurs de transport

Les fournisseurs de transport peuvent utiliser [la fonction BuildDisplayTable](builddisplaytable.md) pour simplifier la construction d’un tableau d’affichage à utiliser avec **DoConfigPropSheet.** Les fournisseurs de transport peuvent également utiliser directement l’API de feuille de propriétés. Pour mettre en mémoire tampon les modifications apportées aux propriétés, les fournisseurs de transport peuvent utiliser [la fonction CreateIProp.](createiprop.md) Cela simplifie la gestion des annulations par l’utilisateur, tandis que l’utilisateur modifie les valeurs stockées dans les propriétés. Si nécessaire, un fournisseur de transport peut également fournir une boîte de dialogue d’Assistant pour simplifier les tâches de configuration de l’utilisateur. 
  

