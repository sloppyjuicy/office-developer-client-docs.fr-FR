---
title: Affichage des feuilles de propriétés de configuration
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: c9386b98-615f-488c-8212-11d9abebbdcf
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: fa48e97ed25fe1175ffd3a92ac961dcf5bde50b4
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22588355"
---
# <a name="displaying-configuration-property-sheets"></a>Affichage des feuilles de propriétés de configuration

**S’applique à**: Outlook 2013 | Outlook 2016 
  
Fournisseurs de transport utilisent la méthode [IMAPISupport::DoConfigPropsheet](imapisupport-doconfigpropsheet.md) pour implémenter des feuilles de propriétés de configuration. Lors de l’appel **DoConfigPropSheet**, le fournisseur de transport transmet un pointeur vers un tableau de propriétés ainsi que des informations sur la façon de les afficher. Ensuite, MAPI présente les propriétés à l’utilisateur au moyen d’une boîte de dialogue standard. Il est vivement recommandé d’utiliser ce mécanisme de feuille de propriété lors de l’implémentation de votre fournisseur de transport en raison de l’avantage pour l’utilisateur d’une interface cohérente.
  
## <a name="transport-providers"></a>Fournisseurs de transport

Fournisseurs de transport peuvent utiliser la fonction [BuildDisplayTable](builddisplaytable.md) pour simplifier la construction d’un tableau d’affichage pour une utilisation avec **DoConfigPropSheet**. Fournisseurs de transport peuvent également utiliser l’API de feuille de propriété directement. Modifications apportées aux propriétés de la mémoire tampon, fournisseurs de transport peut utiliser la fonction [CreateIProp](createiprop.md) . Cela simplifie la gestion des annulations par l’utilisateur pendant que l’utilisateur modifie les valeurs stockées dans les propriétés. Si nécessaire, un fournisseur de transport peut également fournir une boîte de dialogue Assistant case pour simplifier les tâches de configuration de l’utilisateur. 
  

