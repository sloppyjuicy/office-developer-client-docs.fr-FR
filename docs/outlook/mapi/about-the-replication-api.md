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
  
L'API de réPlication fournit les fonctionnalités d'un fournisseur de banque de messages MAPI pour synchroniser les éléments Microsoft Outlook 2013 ou Microsoft Outlook 2010 entre un serveur et un magasin local. pst privé créé pour ce fournisseur. 
  
> [!NOTE]
> Un fournisseur de banque de messages MAPI doit implémenter l'API de réPlication conformément aux instructions de [la rubrique à propos de la machine à États](about-the-replication-state-machine.md)de réplication. Le fournisseur doit utiliser l'API uniquement sur un magasin personnel créé pour lui-même, et non sur des magasins personnels créés pour d'autres fournisseurs, car des magasins personnels créés pour d'autres fournisseurs ont déjà configuré leurs propres mécanismes de réplication avec le serveur respectif. Par exemple, un fichier de dossiers en mode hors connexion (. ost) conserve sa propre relation de réplication avec un serveur Microsoft Exchange. 
  
Pour utiliser l'API de réPlication, un fournisseur de banque de messages MAPI doit d'abord ouvrir et encapsuler un magasin local basé sur un fichier. pst en appelant **[NSTServiceEntry](nstserviceentry.md)**. Le fournisseur peut ensuite utiliser les principales interfaces de l'API **[IOSTX](iostxiunknown.md)** et **[IPSTX](ipstxiunknown.md)** pour effectuer la réplication. **IPSTX** est fourni par l'interrogation sur [IMsgStore: IMAPIProp](imsgstoreimapiprop.md)et **IOSTX** est fourni par **[IPSTX:: GetSyncObject](ipstx-getsyncobject.md)**. 
  
## <a name="the-iostx-interface"></a>Interface IOSTX

L'interface **IOSTX** est l'interface principale qui effectue la synchronisation dans l'API de réplication. **IOSTX** déplace le magasin local par le biais d'une série d'États, en récupérant des informations dans chaque État sur les modifications apportées à la banque locale, ainsi qu'en informant le magasin local des modifications apportées sur le serveur. L'API de réPlication spécifie également de nombreuses structures de données qui prennent en charge la synchronisation. 
  
Un fournisseur de banque, en tant que client pour cette API, utilise l'API de réPlication pour encapsuler le magasin local et parcourir ces États, en envoyant les modifications sur le magasin local (telles que les modifications apportées à la hiérarchie de dossiers ou l'ajout de nouveaux éléments) au serveur et en extrayant également informations sur les modifications sur le serveur et la fourniture de ces informations à l'interface **IOSTX** . L'interface **IOSTX** adopte une synchronisation des modifications incrémentielles fournie par Microsoft Exchange Server. Pour plus d'informations sur le partage de connexion Internet, consultez la rubrique [critères d'évaluation ICS](https://msdn.microsoft.com/library/aa579252%28EXCHG.80%29.aspx). Via **IOSTX**, le client utilise ICS pour surveiller et synchroniser les modifications incrémentielles apportées à la hiérarchie ou au contenu d'un magasin local. 
  
## <a name="the-ipstx-interface"></a>Interface IPSTX

 **IPSTX** et cinq autres * * IPSTX *n* * * les interfaces qui héritent de **IPSTX** fournissent une fonctionnalité d'assistance qui peut être utilisée lors de l'exécution de la réplication via l'interface **IOSTX** . Par exemple, **[IPSTX:: EmulateSpooler](ipstx-emulatespooler.md)** vous permet de faire en sorte que le magasin local émule le gestionnaire de protocoles Outlook pour mettre en file d'attente les messages sortants vers un serveur. 
  
Pour plus d'informations sur les transitions d'état lors de la réplication, voir [à propos de la machine à États](about-the-replication-state-machine.md)de réplication.
  
## <a name="the-replication-api"></a>API de réPlication

L'API de réPlication fournit les defintions, les types de données et les interfaces suivants. Pour un exemple d'implémentation d'un fournisseur de magasin pour les fichiers de dossiers personnels (PST) encapsulés, voir [à propos de l'exemple de fournisseur de magasins PST encapsulé](about-the-sample-wrapped-pst-store-provider.md).
  
Définitions :
  
- [Constantes pour l'API de réPlication](mapi-constants.md)
    
Fonctions :
  
- **[NSTServiceEntry](nstserviceentry.md)**
    
Types de données:
  
- **[DNHIER](dnhier.md)**
    
- **[DNTBL](dntbl.md)**
    
- **[DNTBLE](dntble.md)**
    
- **[FEID](feid.md)**
    
- **[HDRSYNC](hdrsync.md)**
    
- **[LTID](ltid.md)**
    
- **[MEID](meid.md)**
    
- **[OLFI](olfi.md)**
    
- **[SKEY](skey.md)**
    
- **[SYNCHRONI](sync.md)**
    
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
    

