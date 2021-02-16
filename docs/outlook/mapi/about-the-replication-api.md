---
title: À propos de l’API de réplication
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 5133045a-b1e2-7728-5cd5-6d85eb940cf9
description: 'Derni�re modification�: lundi 25 juin 2012'
ms.openlocfilehash: 532c01d6885e72753067b2d30bf2bd5f88207176
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32329518"
---
# <a name="about-the-replication-api"></a>À propos de l’API de réplication

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
L’API de réplication fournit la fonctionnalité permettant à un fournisseur de banque de messages MAPI de synchroniser les éléments Microsoft Outlook 2013 ou Microsoft Outlook 2010 entre un serveur et un magasin local .pst privé créé pour ce fournisseur. 
  
> [!NOTE]
> Un fournisseur de magasin de messages MAPI doit implémenter l’API de réplication conformément aux instructions de la machine à états de [réplication.](about-the-replication-state-machine.md) Le fournisseur doit utiliser l’API uniquement sur un magasin personnel créé pour lui-même, et non sur les magasins personnels créés pour d’autres fournisseurs, car les magasins personnels créés pour d’autres fournisseurs ont peut-être déjà mis en place leurs propres mécanismes de réplication avec le serveur respectif. Par exemple, un fichier de dossier hors connexion (.ost) conserve sa propre relation de réplication avec un serveur Microsoft Exchange. 
  
Pour utiliser l’API de réplication, un fournisseur de magasin de messages MAPI doit d’abord ouvrir et encapsuler un magasin local .pst en appelant **[NSTServiceEntry](nstserviceentry.md)**. Le fournisseur peut ensuite utiliser les interfaces principales de l’API, **[IOSTX](iostxiunknown.md)** et **[IPSTX](ipstxiunknown.md)**, pour effectuer la réplication. **IPSTX est** fourni par l’interrogation sur [IMsgStore : IMAPIProp](imsgstoreimapiprop.md)et **IOSTX** est fourni par **[IPSTX::GetSyncObject](ipstx-getsyncobject.md)**. 
  
## <a name="the-iostx-interface"></a>The IOSTX Interface

**L’interface IOSTX** est l’interface principale qui effectue la synchronisation dans l’API de réplication. **IOSTX** déplace le magasin local par le biais d’une série d’états, en récupérant des informations dans chaque état sur les modifications apportées au magasin local, ainsi qu’en informant le magasin local des modifications sur le serveur. L’API de réplication spécifie également de nombreuses structures de données qui la prise en charge de la synchronisation. 
  
Un fournisseur de magasin, en tant que client de cette API, utilise l’API de réplication pour encapsuler le magasin local et passer par ces états, en pushant les modifications sur le magasin local (telles que les modifications apportées à la hiérarchie de dossiers ou l’ajout de nouveaux éléments) au serveur, et en récupérant également des informations sur les modifications apportées au serveur et en fournissant ces informations à l’interface **IOSTX.** **L’interface IOSTX** adopte la synchronisation des changements incrémentielles (ICS) fournie par Microsoft Exchange Server. Pour plus d’informations sur ICS, voir [critères d’évaluation ICS.](https://msdn.microsoft.com/library/aa579252%28EXCHG.80%29.aspx) Via **IOSTX,** le client utilise ICS pour surveiller et synchroniser les modifications incrémentielles apportées à la hiérarchie ou au contenu sur un magasin local. 
  
## <a name="the-ipstx-interface"></a>The IPSTX Interface

 **IPSTX** et cinq autres interfaces **IPSTX *n* ** qui héritent **d’IPSTX** fournissent des fonctionnalités d’aide qui peuvent être utilisées lors de la réplication via l’interface **IOSTX.** Par exemple, **[IPSTX::EmulateSpooler](ipstx-emulatespooler.md)** vous permet de faire en sorte que le magasin local émule le Gestionnaire de protocole Outlook pour qu’il stocke des messages sortants sur un serveur. 
  
Pour plus d’informations sur les transitions d’état pendant la réplication, voir À propos de [la machine à états de réplication.](about-the-replication-state-machine.md)
  
## <a name="the-replication-api"></a>API de réplication

L’API de réplication fournit les définitions, les types de données et les interfaces suivants. Pour un exemple d’implémentation d’un fournisseur de magasin pour les fichiers de dossiers personnels wrapped (PST), voir à propos de l’exemple de fournisseur de magasin [PST Wrapped](about-the-sample-wrapped-pst-store-provider.md).
  
Définitions :
  
- [Constantes de l’API de réplication](mapi-constants.md)
    
Fonctions :
  
- **[NSTServiceEntry](nstserviceentry.md)**
    
Types de données :
  
- **[DNHIER](dnhier.md)**
    
- **[DNTBL](dntbl.md)**
    
- **[DNTBLE](dntble.md)**
    
- **[FEID](feid.md)**
    
- **[HDRSYNC](hdrsync.md)**
    
- **[LTID](ltid.md)**
    
- **[MEID](meid.md)**
    
- **[OLFI](olfi.md)**
    
- **[SKEY](skey.md)**
    
- **[SYNC](sync.md)**
    
- **[SYNCCONT](synccont.md)**
    
- **[SYNCSTATE](syncstate.md)**
    
- **[UPDEL](updel.md)**
    
- **[UPDELE](updele.md)**
    
- **[UPFLD](upfld.md)**
    
- **[UPHIER](uphier.md)**
    
- **[UPMOV](upmov.md)**
    
- **[UPMSG](upmsg.md)**
    
- **[UPREAD](upread.md)**
    
- **[UPREADE](upreade.md)**
    
- **[UPTBL](uptbl.md)**
    
- **[UPTBLE](uptble.md)**
    
Interfaces :
  
- **[IOSTX](iostxiunknown.md)**
    
- **[IPSTX](ipstxiunknown.md)**
    
- **[IPSTX2](ipstx2ipstx.md)**
    
- **[IPSTX3](ipstx3ipstx2.md)**
    
- **[IPSTX4](ipstx4ipstx3.md)**
    
- **[IPSTX5](ipstx5ipstx4.md)**
    
- **[IPSTX6](ipstx6ipstx5.md)**
    

