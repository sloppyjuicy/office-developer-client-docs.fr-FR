---
title: Gestion de la mémoire dans MAPI
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 9eee6925-ab91-413e-8907-c747ab4a4bb5
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: c30aa631e70f8f4be52c2fd42dd6bfad900f379e
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22566158"
---
# <a name="managing-memory-in-mapi"></a>Gestion de la mémoire dans MAPI

  
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
Savoir quand et comment allouer et libérer de la mémoire constitue une part importante de la programmation MAPI. MAPI fournit les fonctions et les macros que votre client ou fournisseur de services permettre utiliser pour gérer la mémoire de façon cohérente. Les trois fonctions sont les suivantes :
  
[MAPIAllocateBuffer](mapiallocatebuffer.md)
  
[MAPIAllocateMore](mapiallocatemore.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
Lorsque les clients et les fournisseurs de services utilisent ces fonctions, le problème de « propriétaire », c'est-à-dire, sait comment libérer — un bloc de mémoire particulier est éliminé. Un client appelant une méthode de fournisseur de service ne devez pas transmettre un tampon suffisant pour contenir une valeur de retour de toute taille. Le fournisseur de services peut allouer simplement la quantité de mémoire à l’aide de **MAPIAllocateBuffer** appropriée et, si nécessaire, **MAPIAllocateMore**et le client peuvent ultérieurement libérer à l’aide de **MAPIFreeBuffer**, indépendamment du service fournisseur de services. 
  
Les macros de mémoire sont utilisés pour affecter des structures ou des tableaux de structures d’une taille spécifique. Clients et fournisseurs de services doivent utiliser ces macros au lieu d’allouer de la mémoire manuellement. Par exemple, si un client doit effectuer une résolution de traitement sur une liste de destinataires avec trois entrées, la macro **SizedADRLIST** peut être utilisée pour créer une structure **ADRLIST** à transmettre à **IAddrBook::ResolveName** avec le nombre approprié de Membres **ADRENTRY** . Toutes les macros de mémoire sont définies dans le MAPIDEFS. Fichier d’en-tête H. Ces macros sont les suivants : 
  
|||
|:-----|:-----|
|[SizedADRLIST](sizedadrlist.md) <br/> |[SizedDtblPage](sizeddtblpage.md) <br/> |
|[SizedDtblButton](sizeddtblbutton.md) <br/> |[SizedENTRYID](sizedentryid.md) <br/> |
|[SizedDtblCheckBox](sizeddtblcheckbox.md) <br/> |[SizedSPropProblemArray](sizedspropproblemarray.md) <br/> |
|[SizedDtblComboBox](sizeddtblcombobox.md) <br/> |[SizedSPropTagArray](sizedsproptagarray.md) <br/> |
|[SizedDtblEdit](sizeddtbledit.md) <br/> |[SizedSRowSet](sizedsrowset.md) <br/> |
|[SizedDtblGroupBox](sizeddtblgroupbox.md) <br/> |[SizedSSortOrderSet](sizedssortorderset.md) <br/> |
|[SizedDtblLabel](sizeddtbllabel.md) <br/> | <br/> |
   
MAPI prend également en charge l’utilisation de l’interface COM [IMalloc](http://msdn.microsoft.com/en-us/library/ms678425%28VS.85%29.aspx) pour la gestion de la mémoire. Fournisseurs de services figurent un pointeur d’interface **IMalloc** par MAPI lors de l’initialisation et peuvent également récupérer par le biais de la fonction [MAPIGetDefaultMalloc](mapigetdefaultmalloc.md) . Le principal avantage de l’utilisation des méthodes **IMalloc** pour la gestion de la mémoire sur les fonctions MAPI est qu’avec les méthodes COM, il est possible réattribuer un tampon existant. Les fonctions de mémoire MAPI ne prennent pas en charge réaffectation. 
  

