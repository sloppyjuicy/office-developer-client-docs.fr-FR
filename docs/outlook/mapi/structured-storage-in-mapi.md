---
title: Structure Stockage mapi
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 642a678b-4bf2-4246-85cb-c798de23e36f
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: dcbd61a8d5fe3f18fabf9e33a530662a1b6199f0
ms.sourcegitcommit: c0fae34cd3a9c75a7cffcf9ae8e417ddde07a989
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/12/2022
ms.locfileid: "62771852"
---
# <a name="structured-storage-in-mapi"></a>Structure Stockage mapi

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Le stockage structuré fait référence à l’organisation hiérarchique de stockage introduite avec COM. Dans un environnement de stockage structuré, le stockage est organisé en deux ou trois types d’objets : 
  
- Objets Stream
    
- Verrouiller les objets d’octets
    
- Stockage objets
    
Les octets de flux et de verrouillage sont des objets de niveau inférieur qui accèdent directement aux données. Les objets Stream implémentent l’interface **IStream** qui définit les méthodes de lecture, d’écriture, de positionnement et de copie d’octets de données. Les objets d’octets de verrouillage implémentent une autre interface COM, **ILockBytes**, pour accéder aux données avec un tableau d’octets. Les tableaux d’bytes sont généralement utilisés pour fournir un accès personnalisé au stockage sous-jacent.
  
Stockage objets sont superposés au-dessus du flux ou verrouillent des objets octets ; ils peuvent contenir un ou plusieurs de ces objets, ainsi que d’autres objets de stockage. Stockage implémentent l’interface **IStorage** qui définit les méthodes de création, d’accès et de gestion des objets imbrmbrés. 
  
Étant **donné que IStream**, **ILockBytes** et **IStorage** sont des interfaces COM plutôt que des interfaces MAPI, leurs méthodes retournent des valeurs d’erreur COM plutôt que des valeurs MAPI. Les clients et fournisseurs de services appelant des méthodes dans ces interfaces doivent utiliser la fonction API **MapStorageSCode** pour traduire ces valeurs en valeurs d’erreur MAPI. Pour plus d’informations, [voir MapStorageSCode](mapstoragescode.md).
  
Les clients et les fournisseurs de services utilisent un stockage structuré pour utiliser des propriétés trop grandes pour être utilisées avec les méthodes **IMAPIProp** , généralement des propriétés binaires et de chaîne de grande taille. L’un des moyens courants d’accès des clients ou des fournisseurs de services consiste à spécifier **IStream** ou **IStorage** comme identificateur d’interface dans un appel à la méthode [IMAPIProp::OpenProperty](imapiprop-openproperty.md) . Par exemple, les clients appellent **OpenProperty** avec **PR_ATTACH_DATA_BIN** comme balise de propriété et IID_IStream comme identificateur d’interface pour accéder à une pièce jointe binaire dans un message. 
  
Les clients et les fournisseurs de services peuvent implémenter leurs propres objets de flux et de stockage, ou appeler des fonctions d’API pour accéder aux implémentations fournies par MAPI ou COM. Étant donné que les implémentations fournies servent la plupart des objectifs, les clients et les fournisseurs de services ont rarement besoin de créer leurs propres implémentations. 
  
Lorsqu’un client appelle **OpenProperty** sur un objet MAPI pour accéder à l’une de ses propriétés via un objet de stockage, le fournisseur de services ouvre généralement l’objet de stockage en mode direct. Toutefois, il s’agit d’un comportement classique plutôt que obligatoire. Les clients doivent supposer que tous les objets de stockage ouverts ou créés par des fournisseurs de services sont transposés et nécessitent un appel à **IStorage::Commit**. Ils doivent également se souvenir que les modifications apportées aux objets de stockage ne seront pas définitives tant qu’ils n’appelleront **pas IMAPIProp::SaveChanges** après la validation finale pour enregistrer l’objet MAPI. Pour plus d’informations, [voir IMAPIProp::SaveChanges](imapiprop-savechanges.md).
  
MAPI et COM fournissent plusieurs fonctions API pour définir ou accéder aux objets de stockage et de flux. Les fonctions couramment utilisées sont décrites dans le tableau suivant.
  
**Fonctions pour accéder aux objets Stockage et Stream**

|**Fonction**|**Description**|
|:-----|:-----|
|[HrIStorageFromStream](hristoragefromstream.md) <br/> |Crée un objet de stockage pour accéder à un flux ou verrouiller un objet octets. |
|[OpenIMsgOnIStg](openimsgonistg.md) <br/> |Crée un objet message pour accéder à un objet de stockage. |
|[OpenStreamOnFile](openstreamonfile.md) <br/> |Crée un objet de flux pour accéder à un fichier. |
|[WrapCompressedRTFStream](wrapcompressedrtfstream.md) <br/> |Crée un objet stream qui contient la version compressée ou non compressée d’un flux contenant le texte enrichi d’un message. |
   
 **Pour récupérer les noms des flux dans un sous-torage donné**
  
1. Appelez la méthode **IStorage::EnumElements** du sous-torage pour obtenir une interface **IEnumSTATSTG** . 
    
2. **Appelez IEnumSTATSTG::Next** avec autant de structures **STATSTG** à la fois que possible. Si vous demandez 100 à la fois, **Next** retourne généralement S_FALSE dont le contenu  _de pceltFetched_ est le nombre réellement récupéré. 
    
3. Recherchez les structures **STATSTG** marquées avec STGTY_STREAM. 
    
4. Relâchez  _le paramètre pwcsName_ . 
    
 **Pour créer un objet de stockage pour accéder à un flux existant ou verrouiller un objet octets**
  
- Les clients [appellent HrIStorageFromStream](hristoragefromstream.md). 
    
 **Pour créer un objet message pour accéder à un objet de stockage existant**
  
- Les fournisseurs de services et les clients [appellent OpenIMsgOnIStg](openimsgonistg.md). L’objet de message créé diffère des objets de message généralement créés par les fournisseurs de magasins de messages dans la mesure où il ne prend pas en charge toutes les méthodes d’interface [IMessage : IMAPIProp](imessageimapiprop.md) , telles que **IMessage::SubmitMessage**. Un paramètre d’entrée facultatif pour **OpenIMsgOnIStg** est une fonction de rappel conforme au prototype [MSGCALLRELEASE](msgcallrelease.md) . Cette fonction est appelée par le nouvel objet message lorsque le nombre de références du message atteint zéro. **L’implémentation d’une fonction MSGCALLRELEASE** peut être utile pour effectuer un traitement final avant la suppression complète du nouveau message. 
    
[OpenStreamOnFile est](openstreamonfile.md) couramment utilisé pour le stockage des pièces jointes, car il crée un flux qui lit et écrit dans un fichier. **OpenProperty** avec **PR_ATTACH_DATA_BIN** la balise de propriété crée un flux pour le stockage des données de pièces jointes binaires. 
  
 **Pour compresser ou décompresser un flux contenant du texte de message au format Texte enrichi**
  
- Les clients [appellent WrapCompressedRTFStream](wrapcompressedrtfstream.md). **WrapCompressedRTFStream** crée un flux qui enveloppe le flux RTF. Le flux wrapper n’implémente pas toutes les **méthodes IStream** ; les méthodes suivantes sont exclues : **Seek**, **SetSize**, **Revert**, **LockRegion**, **UnlockRegion**, **Stat** et **Clone**. Cela est dû au fait que les objets de flux créés par **WrapCompressedRTFStream** ne prendre en charge **ni SetSize** ni **Stat**, il n’existe pas de moyen simple d’étendre ou de récupérer leur taille. La meilleure stratégie consiste à sélectionner une taille de mémoire tampon raisonnable et à lire ou écrire dans une boucle.
    
> [!NOTE]
> COM a une implémentation d’objet de stockage basée sur un tableau d’byte qui renvoie un objet **IEnumSTATSTG** à partir de la méthode **EnumElements** qui pose problème. En particulier, la **méthode QueryInterface** ne fonctionne pas correctement. Les fournisseurs de services qui implémentent leurs propres objets de stockage à l’aide de l’implémentation COM doivent créer un wrapper fin pour l’objet **IEnumSTATSTG** qui forwarde les appels aux méthodes **IEnumSTATSTG** sous-jacentes, mais implémente ses propres méthodes **AddRef**, **Release**, **QueryInterface** et **Clone** . 
  

