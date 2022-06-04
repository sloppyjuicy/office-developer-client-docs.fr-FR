---
title: Stockage structuré dans MAPI
description: Décrit comment, dans un environnement de stockage structuré, le stockage est organisé en deux ou trois types d’objets.
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 642a678b-4bf2-4246-85cb-c798de23e36f
ms.openlocfilehash: 5c8bfdaa8e9bdef9c910a5eff970be1a830d10fe
ms.sourcegitcommit: eb83b72d14a07ac316c71e8208397d1c7046f6df
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/04/2022
ms.locfileid: "65893675"
---
# <a name="structured-storage-in-mapi"></a>Stockage structuré dans MAPI

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Le stockage structuré fait référence à l’organisation hiérarchique du stockage introduite avec COM. Dans un environnement de stockage structuré, le stockage est organisé en deux ou trois types d’objets : 
  
- Diffuser des objets
    
- Verrouiller des objets d’octets
    
- Objets de stockage
    
Les octets de flux et de verrouillage sont des objets de niveau inférieur qui accèdent directement aux données. Les objets Stream implémentent l’interface **IStream** qui définit des méthodes pour la lecture, l’écriture, le positionnement et la copie d’octets de données. Les objets de verrouillage d’octets implémentent une autre interface COM, **ILockBytes**, pour accéder aux données avec un tableau d’octets. Les tableaux d’octets sont généralement utilisés pour fournir un accès personnalisé au stockage sous-jacent.
  
Les objets de stockage sont superposés au-dessus des objets de flux ou d’octets de verrouillage ; ils peuvent contenir un ou plusieurs de ces objets ainsi que d’autres objets de stockage. Les objets de stockage implémentent l’interface **IStorage** qui définit des méthodes pour la création, l’accès et la maintenance d’objets imbriqués. 
  
Étant donné que **IStream**, **ILockBytes** et **IStorage** sont des interfaces COM plutôt que des interfaces MAPI, leurs méthodes retournent des valeurs d’erreur COM plutôt que des valeurs MAPI. Les clients et les fournisseurs de services appelant des méthodes dans ces interfaces doivent utiliser la fonction API **MapStorageSCode** pour traduire ces valeurs en valeurs d’erreur MAPI. Pour plus d’informations, consultez [MapStorageSCode](mapstoragescode.md).
  
Les clients et les fournisseurs de services utilisent un stockage structuré pour utiliser des propriétés trop volumineuses pour être conservées avec les méthodes **IMAPIProp** , généralement des propriétés binaires et de chaîne volumineuses. L’une des façons courantes d’accéder aux clients ou aux fournisseurs de services consiste à spécifier **IStream** ou **IStorage** comme identificateur d’interface dans un appel à la méthode [IMAPIProp::OpenProperty](imapiprop-openproperty.md) . Par exemple, les clients appellent **OpenProperty** avec **PR_ATTACH_DATA_BIN** comme balise de propriété et IID_IStream comme identificateur d’interface pour accéder à une pièce jointe binaire dans un message. 
  
Les clients et les fournisseurs de services peuvent implémenter leurs propres objets de flux et de stockage ou appeler des fonctions API pour accéder aux implémentations fournies par MAPI ou COM. Étant donné que les implémentations fournies servent la plupart des objectifs, les clients et les fournisseurs de services ont rarement besoin de créer leurs propres implémentations. 
  
Lorsqu’un client appelle **OpenProperty** sur un objet MAPI pour accéder à l’une de ses propriétés via un objet de stockage, le fournisseur de services ouvre généralement l’objet de stockage en mode direct. Toutefois, il s’agit d’un comportement classique plutôt que obligatoire. Les clients doivent supposer que tous les objets de stockage ouverts ou créés par les fournisseurs de services sont transactionnels et nécessitent un appel à **IStorage::Commit**. Ils doivent également se rappeler que les modifications apportées aux objets de stockage ne seront pas rendues permanentes tant qu’ils n’auront pas appelé **IMAPIProp::SaveChanges** après **la validation finale** pour enregistrer l’objet MAPI. Pour plus d’informations, consultez [IMAPIProp::SaveChanges](imapiprop-savechanges.md).
  
MAPI et COM fournissent plusieurs fonctions API pour la définition ou l’accès aux objets de stockage et de flux. Les fonctions couramment utilisées sont décrites dans le tableau suivant.
  
**Fonctions permettant d’accéder aux objets de stockage et de flux**

|**Fonction**|**Description**|
|:-----|:-----|
|[HrIStorageFromStream](hristoragefromstream.md) <br/> |Crée un objet de stockage pour accéder à un objet de flux ou d’octets de verrouillage. |
|[OpenIMsgOnIStg](openimsgonistg.md) <br/> |Crée un objet de message pour accéder à un objet de stockage. |
|[OpenStreamOnFile](openstreamonfile.md) <br/> |Crée un objet de flux pour accéder à un fichier. |
|[WrapCompressedRTFStream](wrapcompressedrtfstream.md) <br/> |Crée un objet de flux qui contient la version compressée ou non compressée d’un flux contenant le texte enrichi d’un message. |
   
 **Pour récupérer les noms des flux dans un sous-magasin donné**
  
1. Appelez la méthode **IStorage::EnumElements** du sous-magasin pour obtenir une interface **IEnumSTATSTG** . 
    
2. Appelez **IEnumSTATSTG::Next** avec autant de structures **STATSTG** à la fois que possible. Si vous demandez 100 à la fois, **Next** retourne généralement S_FALSE avec le contenu de  _pceltFetched_ défini sur le nombre qui ont été réellement récupérés. 
    
3. Recherchez les structures **STATSTG** marquées avec STGTY_STREAM. 
    
4. Relâchez le paramètre  _pwcsName_ . 
    
 **Pour créer un objet de stockage pour accéder à un flux existant ou à un objet d’octets de verrouillage**
  
- Les clients appellent [HrIStorageFromStream](hristoragefromstream.md). 
    
 **Pour créer un objet de message pour accéder à un objet de stockage existant**
  
- Les fournisseurs de services et les clients appellent [OpenIMsgOnIStg](openimsgonistg.md). L’objet de message créé diffère des objets de message généralement créés par les fournisseurs de magasins de messages, car il ne prend pas en charge toutes les méthodes d’interface [IMessage : IMAPIProp](imessageimapiprop.md) , telles que **IMessage::SubmitMessage**. Un paramètre d’entrée facultatif pour **OpenIMsgOnIStg** est une fonction de rappel qui est conforme au prototype [MSGCALLRELEASE](msgcallrelease.md) . Cette fonction est appelée par le nouvel objet de message lorsque le nombre de références du message atteint zéro. L’implémentation d’une fonction **MSGCALLRELEASE** peut être utile pour effectuer le traitement final avant la suppression complète du nouveau message. 
    
[OpenStreamOnFile](openstreamonfile.md) est couramment utilisé pour stocker des pièces jointes de fichier, car il crée un flux qui lit et écrit dans un fichier. **OpenProperty** avec **PR_ATTACH_DATA_BIN** comme balise de propriété crée un flux pour le stockage des données de pièce jointe binaire. 
  
 **Pour compresser ou décompresser un flux contenant du texte de message au format texte enrichi**
  
- Les clients appellent [WrapCompressedRTFStream](wrapcompressedrtfstream.md). **WrapCompressedRTFStream** crée un flux qui encapsule le flux RTF. Le flux de wrapper n’implémente pas toutes les méthodes **IStream** ; les méthodes suivantes sont exclues : **Seek**, **SetSize**, **Revert**, **LockRegion**, **UnlockRegion**, **Stat** et **Clone**. En raison du fait que les objets de flux créés par **WrapCompressedRTFStream** ne prennent pas en charge **SetSize** ou **Stat**, il n’existe pas de moyen simple d’étendre ou de récupérer leur taille. La meilleure stratégie consiste à choisir une taille de mémoire tampon raisonnable et à lire ou écrire dans une boucle.
    
> [!NOTE]
> COM a une implémentation d’objet de stockage basée sur un tableau d’octets qui retourne un objet **IEnumSTATSTG** à partir de la méthode **EnumElements** qui pose problème. En particulier, la méthode **QueryInterface** ne fonctionne pas correctement. Les fournisseurs de services qui implémentent leurs propres objets de stockage à l’aide de l’implémentation COM doivent créer un wrapper fin pour l’objet **IEnumSTATSTG** qui transfère les appels aux méthodes **IEnumSTATSTG** sous-jacentes, mais implémente ses propres méthodes **AddRef**, **Release**, **QueryInterface** et **Clone** . 
  

