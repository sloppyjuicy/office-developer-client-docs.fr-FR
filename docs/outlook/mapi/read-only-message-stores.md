---
title: Banques de messages en lecture seule
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 752ff2d6-ca64-4507-adf1-4c054c321203
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: 957a7f92963b97e5421bc801a3b046f098d6a08e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33405337"
---
# <a name="read-only-message-stores"></a>Banques de messages en lecture seule

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Une banque de messages en lecture seule est une dans laquelle ni le client MAPI, ni le spouleur MAPI peut cr�er, modifier ou supprimer les objets de la banque de messages. Il existe plusieurs raisons peuvent expliquer pourquoi vous souhaiterez peut-�tre mettre en �uvre une banque de messages en lecture seule. Par exemple, un cabinet de cr�ation de rapports de cr�dit peut utiliser un magasin en lecture seule pour permettre � ses clients ou des employ�s � voir, mais ne modifie pas les rapports de cr�dit individuels. Possibilit� de rendre un message en lecture seule � stocker a des cons�quences de la structure du fournisseur de banque et de la banque elle-m�me. Par exemple, une banque de messages en lecture seule n'est pas un dossier bo�te d'envoi, car, puis les clients MAPI demandait que les nouveaux messages sortants �tre cr��s dans ce dossier. De m�me, il incombe au fournisseur de magasin afin de garantir l'int�grit� du m�canisme de stockage sous-jacent.
  
Il existe trois indicateurs qui peuvent être définies dans la propriété **PR_STORE_SUPPORT_MASK** [(PidTagStoreSupportMask)](pidtagstoresupportmask-canonical-property.md)de la boutique de messages qui prendre en charge différents niveaux d’accès en lecture seule. The STORE_READONLY flag indicates that all [IMAPIProp : IUnknown](imapipropiunknown.md) interfaces on objects in the message store are read-only. The STORE_MODIFY_OK flag indicates that existing messages in the message store may be modified, but new folders and messages may not be created. The STORE_CREATE_OK flag indicates that new messages and folders may be created, but indicates nothing about whether existing objects may be modified. 
  
Le fait que les clients MAPI et le spouleur MAPI ne peuvent pas �tre en mesure de cr�er, modifier ou supprimer des objets dans la banque de messages ne signifie pas que le contenu du m�canisme de stockage sous-jacent change jamais. Ni, cela signifie que votre fournisseur de magasin doit jamais autorisations en �criture pour le m�canisme de stockage sous-jacent. Dans certaines circonstances ces deux conditions peuvent appliquer, mais pas dans le cas g�n�ral d'un message en lecture seule stocker. Le niveau d'acc�s que requiert votre fournisseur de magasins et ou non votre fournisseur de magasin de modification des donn�es dans le m�canisme de stockage sous-jacent d�pend essentiellement de la nature sp�cifique de votre fournisseur de magasins.
  
Par exemple, si vous �crivez un fournisseur de magasins pour donner des clients MAPI l'acc�s � une base de donn�es stock�e sur un lecteur de CD-ROM, le m�canisme de stockage sous-jacent ne peut pas modifier et votre fournisseur de magasin peut avoir l'autorisation en lecture seule. Si, toutefois, vous �crivez un fournisseur de magasins pour permettre aux clients MAPI un acc�s en lecture seule pour une base de donn�es de dossiers publics, mais le fournisseur de magasins doit assurer le suivi de l'�tat lu/des messages pour chaque utilisateur, le fournisseur de banque vous devrez �crire les nouvelles donn�es dans le m�canisme de stockage sous-jacent. Toutefois, ni exemple le fournisseur de banque jamais doit cr�er, modifier ou supprimer des dossiers ou des messages � la demande des clients MAPI ou le spouleur MAPI.
  
La courte liste des raisons pour lesquelles un fournisseur de magasins aurais besoin pour �crire des donn�es � un m�canisme de stockage sous-jacent est en lecture seule est comme suit :
  
- Pour stocker l'�tat lu/des messages.
    
- Pour impl�menter des notifications de lecture/suppression du mode lecture. 
    
- Pour stocker les affichages.
    
- Pour mettre en cache index permanents pour les ordres de tri de dossier d�fini par l'utilisateur.
    
- To store the sort order of a folder's contents (supporting [IMAPIFolder::SaveContentsSort](imapifolder-savecontentssort.md)).
    
- To store search criteria, search state, and results, if the message store provider supports searches (supporting [IMAPIContainer::SetSearchCriteria](imapicontainer-setsearchcriteria.md)).
    
Si votre fournisseur de banque de messages peut jamais �crire des donn�es dans le m�canisme de stockage sous-jacent, qu'elle a besoin impl�menter ces fonctionnalit�s � l'aide d'un m�canisme de stockage distinct � l'ext�rieur du m�canisme de stockage sous-jacent. Par exemple, un fournisseur de magasin de message en lecture seule peut stocker l'�tat lu/des messages dans le magasin dans un fichier sur l'ordinateur de l'utilisateur. Cette strat�gie pr�sente des difficult�s suppl�mentaires, mais sans doute la fa�on de mesure du possible uniquement pour les messages en lecture seule � mettre en �uvre de certaines fonctionnalit�s, les fournisseurs de magasins. Par exemple, en conservant le contenu du dispositif de stockage distincts synchronis� avec les objets de la banque de messages est plus difficile que le stockage de l'�tat lu/directement dans la banque de messages proprement dit.
  
Recherche pr�sente une complication suppl�mentaire pour les fournisseurs de banque de message en lecture seule. Clients use the folder specified in the message store object’s **PR_FINDER_ENTRYID** ([PidTagFinderEntryId](pidtagfinderentryid-canonical-property.md)) property to locate the folder used for search results. Les fournisseurs de banque de message en lecture seule souvent impossible d'installer un dossier permanent de r�sultats de recherche dans la banque de messages. Dans ce cas, le fournisseur de banque de messages doit stocker un identificateur d'entr�e dans la propri�t� **PR_FINDER_ENTRYID** qu'il peut reconna�tre lorsque les clients ouvrent les dossiers afin qu'elle peut cr�er dynamiquement un dossier de r�sultats de recherche au lieu de lire une dans le m�canisme de stockage sous-jacent. Toutefois, �tant donn� que de nombreux fournisseurs de banque de message en lecture seule cr�ent dynamiquement tous leurs dossiers, il s'agit g�n�ralement pas trop lourde. 
  
Le fait que votre fournisseur de banque de messages est en lecture seule est publi� dans la propri�t� **PR_STORE_SUPPORT_MASK** de l'objet fournisseur de magasins. Toutefois, ne sont pas sur les clients de respecter cette propri�t� ; code de votre fournisseur magasin doit appliquer l'�tat en lecture seule du m�canisme de stockage sous-jacent. 
  
## <a name="see-also"></a>Voir aussi



[Développement d’un fournisseur de banque de messages MAPI](developing-a-mapi-message-store-provider.md)

