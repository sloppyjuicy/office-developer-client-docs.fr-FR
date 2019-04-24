---
title: Gestion de la mémoire dans MAPI
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 9eee6925-ab91-413e-8907-c747ab4a4bb5
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 66489c09be641d8fe9ae5f3ffff46a6d5004f473
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32298095"
---
# <a name="managing-memory-in-mapi"></a>Gestion de la mémoire dans MAPI

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Savoir comment et quand allouer et libérer de la mémoire est une partie importante de la programmation avec MAPI. MAPI fournit à la fois des fonctions et des macros que votre client ou fournisseur de services peut utiliser pour gérer la mémoire de manière cohérente. Les trois fonctions sont les suivantes:
  
[MAPIAllocateBuffer](mapiallocatebuffer.md)
  
[MAPIAllocateMore](mapiallocatemore.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
Lorsque les clients et les fournisseurs de services utilisent ces fonctions, le «propriétaire» (c'est-à-dire, dont il est question) sait comment lancer un bloc de mémoire particulier. Un client appelant une méthode de fournisseur de services n'a pas besoin de transmettre un tampon assez grand pour contenir une valeur de retour de n'importe quelle taille. Le fournisseur de services peut simplement allouer la quantité de mémoire appropriée à l'aide de **MAPIAllocateBuffer** et, si nécessaire, **MAPIAllocateMore**, et le client peut le libérer ultérieurement à l'aide de **MAPIFreeBuffer**, indépendamment du service moteur. 
  
Les macros de mémoire sont utilisées pour allouer des structures ou des tableaux de structures d'une taille spécifique. Les clients et les fournisseurs de services doivent utiliser ces macros au lieu d'allouer manuellement la mémoire. Par exemple, si un client doit exécuter le traitement de la résolution de noms sur une liste de destinataires avec trois entrées, la macro **SizedADRLIST** peut être utilisée pour créer une structure **ADRLIST** à transmettre à **IAddrBook:: ResolveName** avec le nombre correct de Membres **ADRENTRY** . Toutes les macros de mémoire sont définies dans le MAPIDEFS. Fichier d'en-tête H. Ces macros sont les suivantes: 
  
|||
|:-----|:-----|
|[SizedADRLIST](sizedadrlist.md) <br/> |[SizedDtblPage](sizeddtblpage.md) <br/> |
|[SizedDtblButton](sizeddtblbutton.md) <br/> |[SizedENTRYID](sizedentryid.md) <br/> |
|[SizedDtblCheckBox](sizeddtblcheckbox.md) <br/> |[SizedSPropProblemArray](sizedspropproblemarray.md) <br/> |
|[SizedDtblComboBox](sizeddtblcombobox.md) <br/> |[SizedSPropTagArray](sizedsproptagarray.md) <br/> |
|[SizedDtblEdit](sizeddtbledit.md) <br/> |[SizedSRowSet](sizedsrowset.md) <br/> |
|[SizedDtblGroupBox](sizeddtblgroupbox.md) <br/> |[SizedSSortOrderSet](sizedssortorderset.md) <br/> |
|[SizedDtblLabel](sizeddtbllabel.md) <br/> | <br/> |
   
MAPI prend également en charge l'utilisation de l' [](https://msdn.microsoft.com/library/ms678425%28VS.85%29.aspx) interface com IMalloc pour la gestion de la mémoire. Les fournisseurs de services reçoivent **** un pointeur d'interface IMalloc par MAPI au moment de l'initialisation et peuvent également en récupérer un par le biais de la fonction [MAPIGetDefaultMalloc](mapigetdefaultmalloc.md) . Le principal avantage de l'utilisation **** des méthodes IMalloc pour la gestion de la mémoire sur les fonctions MAPI est qu'avec les méthodes com, il est possible de réaffecter une mémoire tampon existante. Les fonctions de mémoire MAPI ne prennent pas en charge la réallocation. 
  

