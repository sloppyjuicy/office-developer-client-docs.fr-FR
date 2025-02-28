---
title: Gestion de la mémoire dans MAPI
description: MAPI fournit des fonctions et des macros que votre client ou fournisseur de services peut utiliser pour gérer la mémoire de manière cohérente.
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 9eee6925-ab91-413e-8907-c747ab4a4bb5
ms.openlocfilehash: b6f3845179abf38d8875f2a18ddaa8393b50e519
ms.sourcegitcommit: f872848fbeb5b2353179ad4bf4eab23f61f87666
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/01/2022
ms.locfileid: "65816275"
---
# <a name="managing-memory-in-mapi"></a>Gestion de la mémoire dans MAPI

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Savoir comment et quand allouer et libérer de la mémoire est une partie importante de la programmation avec MAPI. MAPI fournit des fonctions et des macros que votre client ou fournisseur de services peut utiliser pour gérer la mémoire de manière cohérente. Les trois fonctions sont les suivantes :
  
[MAPIAllocateBuffer](mapiallocatebuffer.md)
  
[MAPIAllocateMore](mapiallocatemore.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
Lorsque les clients et les fournisseurs de services utilisent ces fonctions, la question de savoir qui est le « propriétaire » (autrement dit, sait comment libérer) d’un bloc de mémoire particulier est éliminé. Un client appelant une méthode de fournisseur de services n’a pas besoin de passer une mémoire tampon suffisamment grande pour contenir une valeur de retour de n’importe quelle taille. Le fournisseur de services peut simplement allouer la quantité de mémoire appropriée à l’aide de **MAPIAllocateBuffer** et, si nécessaire, **MAPIAllocateMore**, et le client peut la libérer ultérieurement à volonté à l’aide de **MAPIFreeBuffer**, indépendamment du fournisseur de services. 
  
Les macros mémoire sont utilisées pour allouer des structures ou des tableaux de structures d’une taille spécifique. Les clients et les fournisseurs de services doivent utiliser ces macros plutôt que d’allouer la mémoire manuellement. Par exemple, si un client doit effectuer le traitement de résolution de noms sur une liste de destinataires avec trois entrées, la macro **SizedADRLIST** peut être utilisée pour créer une structure **ADRLIST** à passer à **IAddrBook::ResolveName** avec le nombre correct de membres **ADRENTRY** . Toutes les macros mémoire sont définies dans MAPIDEFS. Fichier d’en-tête H. Ces macros sont les suivantes : 
  
|Macro |Macro |
|:-----|:-----|
|[SizedADRLIST](sizedadrlist.md) <br/> |[SizedDtblPage](sizeddtblpage.md) <br/> |
|[SizedDtblButton](sizeddtblbutton.md) <br/> |[SizedENTRYID](sizedentryid.md) <br/> |
|[SizedDtblCheckBox](sizeddtblcheckbox.md) <br/> |[SizedSPropProblemArray](sizedspropproblemarray.md) <br/> |
|[SizedDtblComboBox](sizeddtblcombobox.md) <br/> |[SizedSPropTagArray](sizedsproptagarray.md) <br/> |
|[SizedDtblEdit](sizeddtbledit.md) <br/> |[SizedSRowSet](sizedsrowset.md) <br/> |
|[SizedDtblGroupBox](sizeddtblgroupbox.md) <br/> |[SizedSSortOrderSet](sizedssortorderset.md) <br/> |
|[SizedDtblLabel](sizeddtbllabel.md) <br/> | <br/> |
   
MAPI prend également en charge l’utilisation de l’interface [COM IMalloc](https://msdn.microsoft.com/library/ms678425%28VS.85%29.aspx) pour la gestion de la mémoire. Les fournisseurs de services reçoivent un pointeur d’interface **IMalloc** par MAPI au moment de l’initialisation et peuvent également en récupérer un via la fonction [MAPIGetDefaultMalloc](mapigetdefaultmalloc.md) . Le principal avantage de l’utilisation des méthodes **IMalloc** pour gérer la mémoire sur les fonctions MAPI est qu’avec les méthodes COM, il est possible de réallouer une mémoire tampon existante. Les fonctions de mémoire MAPI ne prennent pas en charge la réallocation. 
  

