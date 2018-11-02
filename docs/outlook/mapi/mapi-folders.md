---
title: Dossiers MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 8fac3c92-d2f5-479e-a368-ca82bddd8e30
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: 21b738424b27d3d89d8de84c8c9ff2ff86dd945b
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22564086"
---
# <a name="mapi-folders"></a>Dossiers MAPI

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Les dossiers sont des objets MAPI qui servent � l'unit� d'organisation pour les messages de base. Structure hi�rarchique, les dossiers peuvent contenir des messages et autres dossiers. Dossiers rendent plus facile � trouver et travailler avec des messages.
  
Dossiers impl�mentent l'interface de [IMAPIFolder](imapifolderimapicontainer.md) , lequel indirectement h�rite de l'interface **IUnknown** par le biais de [IMAPIContainer](imapicontainerimapiprop.md) et [IMAPIProp](imapipropiunknown.md) interfaces. Les clients utilisent **IMAPIFolder** pour cr�er, copier et supprimer des messages et des dossiers, pour extraire et d�finir le statut du message et pour d�finir ou effacer l'indicateur de lecture d'un message. Bien que les fournisseurs de banque de messages sont requis pour prendre en charge toutes les m�thodes de **IMAPIFolder**, certaines m�thodes introduisent un degr� de complexit� que les fournisseurs de banque de message peuvent �viter. MAPI enregistre les fournisseurs de banque de messages des t�ches en mettant en �uvre de certaines des fonctionnalit�s plus complexes de dossier dans l'interface [IMAPISupport](imapisupportiunknown.md) . Au lieu d'impl�menter les m�thodes de leur propre copie, par exemple, les fournisseurs de banque de messages peuvent appeler les m�thodes de copie dans l'objet de prise en charge et obtenir les m�mes r�sultats. 
  
Il existe trois types de dossiers :
  
- Dossiers racine.
    
- Dossiers g�n�riques.
    
- Dossiers de recherche
    
Chaque banque de messages a au moins un dossier racine. Le dossier racine s'affiche en haut de la hi�rarchie et contient des messages et autres dossiers. Dossiers racines ne peut pas �tre d�plac�s, copi�s, renomm�s ou supprim�s. Il n'existe qu'un seul dossier racine de chaque banque de messages.
  
La plupart des autres dossiers sont des dossiers g�n�riques. Comme les dossiers racine, g�n�riques dossiers contiennent des messages et autres dossiers. Contrairement aux dossiers racine, ils peuvent �tre d�plac�s, copi�s, renomm�s et supprim�s. Dossiers g�n�riques peuvent �tre cr��s dans le dossier racine ou les autres dossiers g�n�riques. Lorsqu'un client cr�e un dossier g�n�rique dans un autre dossier, le nouveau dossier est appel� un sous-dossier ou un dossier enfant. Le dossier dans lequel se trouve le nouveau dossier est appel� le dossier parent du nouveau dossier. Dossiers g�n�riques qui ont le m�me dossier parent sont appel�s dossiers fr�res. Fr�re et les dossiers non fr�re peut ou ne peut-�tre pas porter un nom unique, fournisseur de magasins en fonction du message. Fournisseurs de magasins de message qui n�cessitent des dossiers fr�res avec des noms uniques � renvoyer la valeur d'erreur MAPI_E_COLLISION lorsqu'un client tente de cr�er deux dossiers portant le m�me nom dans le m�me parent. 
  
Un dossier de recherche contient des liens vers les messages qui correspondent � un ensemble de crit�res pr�d�finis. �tant donn� que les dossiers de recherche contiennent des liens plut�t que les messages r�els, ils sont en effet en lecture seule. Ils ne peuvent pas contenir d'autres dossiers ou avez des messages ou des dossiers de d�placer ou copier des informations. Ils ne peuvent pas avoir de nouveaux messages cr��s dans leur ; et ils eux-m�mes ne peut pas �tre d�plac�s, copi�s ou renomm�s. Lorsqu'un message est supprim� d'un dossier de recherche, elle est r�ellement supprim�e � partir du dossier qui contient le message.
  
Type de dossier est stocké dans la propriété **PR_FOLDER_TYPE** ([PidTagFolderType](pidtagfoldertype-canonical-property.md)). Chaque dossier cette propri�t� a pour valeur FOLDER_GENERIC, FOLDER_ROOT ou FOLDER_SEARCH, en fonction de son type.
  
Chaque dossier poss�de l'identificateur d'une entr�e et une cl� d'enregistrement. L’identificateur d’entrée, **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)), est utilisé par les clients et les fournisseurs de services pour ouvrir le dossier. La clé d’enregistrement, **PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md)), est une valeur binaire qui est utilisée pour comparer le dossier avec les autres dossiers. 
  
Un dossier a d'autres propri�t�s pour identifier la banque de messages et de dossiers connexes. Les propri�t�s suivantes sont requises :
  
- **PR_PARENT_ENTRYID** ([PidTagParentEntryId](pidtagparententryid-canonical-property.md))
    
- **PR_STORE_ENTRYID** ([PidTagStoreEntryId](pidtagstoreentryid-canonical-property.md))
    
- **PR_STORE_RECORD_KEY** ([PidTagStoreRecordKey](pidtagstorerecordkey-canonical-property.md))
    
Certains dossiers prennent en charge la propriété **PR_ACCESS** ([PidTagAccess](pidtagaccess-canonical-property.md)) qui décrit le type d’un utilisateur peut effectuer des opérations. Par exemple, un des param�tres valides pour **PR_ACCESS** est MAPI_ACCESS_DELETE, ce qui indique que le dossier peut �tre supprim�. Un autre param�tre, MAPI_ACCESS_MODIFY, indique que le dossier doit �tre modifiable. 
  
Pour obtenir une liste compl�te des propri�t�s de dossier requis, voir l'interface [IMAPIFolder](imapifolderimapicontainer.md) . 
  
## <a name="see-also"></a>Voir aussi



[D�veloppement d'applications MAPI](mapi-application-development.md)

