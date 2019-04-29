---
title: Stockage structuré dans MAPI
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 642a678b-4bf2-4246-85cb-c798de23e36f
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: f58fa70e98841db5507323a63737f1df6c1b7a6d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33411749"
---
# <a name="structured-storage-in-mapi"></a>Stockage structuré dans MAPI

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Le stockage structuré fait référence à l'organisation hiérarchique de stockage introduite avec COM. Dans un environnement de stockage structuré, le stockage est organisé en deux ou trois types d'objets: 
  
- Objets Stream
    
- Verrouiller les objets bytes
    
- Objets de stockage
    
Les octets Stream et Lock sont des objets de niveau inférieur qui accèdent directement aux données. Les objets Stream implémentent l'interface **IStream** qui définit des méthodes de lecture, d'écriture, de positionnement et de copie des octets de données. Les objets Lock bytes implémentent une autre interface COM, **ILockBytes**, pour accéder aux données à l'aide d'un tableau d'octets. Les tableaux d'octets sont généralement utilisés pour fournir un accès personnalisé au stockage sous-jacent.
  
Les objets de stockage sont superposés par-dessus les objets Stream ou Lock bytes; ils peuvent contenir un ou plusieurs de ces objets, ainsi que d'autres objets de stockage. Les objets de stockage implémentent l'interface **IStorage** qui définit des méthodes de création, d'accès et de gestion des objets imbriqués. 
  
Dans la mesure où **IStream**, **ILockBytes**et **IStorage** sont des interfaces com plutôt que des interfaces MAPI, leurs méthodes renvoient des valeurs d'erreur com plutôt que des valeurs MAPI. Les clients et les fournisseurs de services qui appellent des méthodes dans ces interfaces doivent utiliser la fonction API **MapStorageSCode** pour traduire ces valeurs en valeurs d'erreur MAPI. Pour plus d'informations, consultez la rubrique [MapStorageSCode](mapstoragescode.md).
  
Les clients et les fournisseurs de services utilisent le stockage structuré pour utiliser des propriétés trop volumineuses pour gérer les méthodes **IMAPIProp** , généralement des propriétés binaires et de chaîne de grande taille. L'un des moyens couramment utilisés par les clients ou les fournisseurs de services est de spécifier **IStream** ou **IStorage** en tant qu'identificateur d'interface dans un appel à la méthode [IMAPIProp:: OpenProperty](imapiprop-openproperty.md) . Par exemple, les clients appellent **OpenProperty** avec **PR_ATTACH_DATA_BIN** comme balise de propriété et IID_IStream comme identificateur d'interface pour accéder à une pièce jointe binaire dans un message. 
  
Les clients et les fournisseurs de services peuvent implémenter leurs propres objets de flux et de stockage ou appeler des fonctions d'API d'appel pour accéder aux implémentations fournies par MAPI ou COM. Étant donné que les implémentations fournies servent la plupart des cas, les clients et les fournisseurs de services ont rarement besoin de créer leur propre fonction. 
  
Lorsqu'un client appelle **OpenProperty** sur un objet MAPI pour accéder à l'une de ses propriétés via un objet de stockage, le fournisseur de services ouvre généralement l'objet de stockage en mode direct. Toutefois, il s'agit du comportement habituel plutôt que d'un comportement obligatoire. Les clients doivent supposer que tous les objets de stockage ouverts ou créés par les fournisseurs de services sont traités et nécessitent un appel à **IStorage:: Commit**. Ils doivent également se rappeler que les modifications apportées aux objets de stockage ne seront pas permanentes tant qu'ils n'auront pas appelé **IMAPIProp:: SaveChanges** après la **validation** finale pour enregistrer l'objet MAPI. Pour plus d'informations, voir [IMAPIProp:: SaveChanges](imapiprop-savechanges.md).
  
MAPI et COM fournissent plusieurs fonctions d'API pour la définition ou l'accès aux objets de stockage et de flux. Les fonctions couramment utilisées sont décrites dans le tableau suivant.
  
**Fonctions d'accès aux objets de stockage et de flux**

|**Fonction**|**Description**|
|:-----|:-----|
|[HrIStorageFromStream](hristoragefromstream.md) <br/> |Crée un objet de stockage pour accéder à un objet Stream ou Lock bytes.  <br/> |
|[OpenIMsgOnIStg](openimsgonistg.md) <br/> |Crée un objet message pour accéder à un objet de stockage.  <br/> |
|[OpenStreamOnFile](openstreamonfile.md) <br/> |Crée un objet Stream pour accéder à un fichier.  <br/> |
|[WrapCompressedRTFStream](wrapcompressedrtfstream.md) <br/> |Crée un objet Stream qui contient la version compressée ou non compressée d'un flux contenant le texte enrichi d'un message.  <br/> |
   
 **Pour récupérer les noms des flux dans un sous-stockage donné**
  
1. Appelez la méthode **IStorage:: EnumElements** du sous-stockage pour obtenir une interface **IEnumSTATSTG** . 
    
2. Appelez **IEnumSTATSTG:: Next** avec autant de structures **STATSTG** à la fois que vous le pouvez. Si vous demandez 100 à la fois, le **suivant** RENVERRA généralement S_FALSE avec le contenu de _pceltFetched_ défini sur le nombre réellement extrait. 
    
3. Vérifiez si les structures **STATSTG** sont marquées avec STGTY_STREAM. 
    
4. Libérez le paramètre _pwcsName_ . 
    
 **Pour créer un objet de stockage pour accéder à un objet Stream ou Lock existant**
  
- Les clients appellent [HrIStorageFromStream](hristoragefromstream.md). 
    
 **Pour créer un objet message pour accéder à un objet de stockage existant**
  
- Les fournisseurs de services et les clients appellent [OpenIMsgOnIStg](openimsgonistg.md). L'objet message créé diffère des objets message généralement créés par les fournisseurs de banque de messages dans la mesure où il ne prend pas en charge toutes les méthodes d'interface [IMessage: IMAPIProp](imessageimapiprop.md) , telles que **IMessage:: SubmitMessage**. Un paramètre d'entrée facultatif vers **OpenIMsgOnIStg** est une fonction de rappel conforme au prototype [MSGCALLRELEASE](msgcallrelease.md) . Cette fonction est appelée par le nouvel objet message lorsque le nombre de référence du message atteint zéro. L'implémentation d'une fonction **MSGCALLRELEASE** peut être utile pour effectuer le traitement final avant la suppression complète du nouveau message. 
    
[OpenStreamOnFile](openstreamonfile.md) est couramment utilisé pour le stockage des pièces jointes, car il crée un flux qui lit et écrit dans un fichier. **OpenProperty** avec **PR_ATTACH_DATA_BIN** comme balise property crée un flux pour le stockage des données de pièces jointes binaires. 
  
 **Pour compresser ou décompresser un flux contenant du texte de message au format RTF**
  
- Les clients appellent [WrapCompressedRTFStream](wrapcompressedrtfstream.md). **WrapCompressedRTFStream** crée un flux qui encapsule le flux RTF. Le flux de wrapper n'implémente pas toutes les méthodes **IStream** ; les méthodes suivantes sont exclues: **Seek**, **** admettent, Revert, **LockRegion**, **UnlockRegion**, **** **Stat**et **clone**. Cela est dû au fait que les objets Stream créés par **WrapCompressedRTFStream** ne **** prennent pas en charge la méthode size ou **Stat**, mais il n'existe pas de moyen facile d'étendre ou de récupérer leur taille. La meilleure stratégie consiste à choisir une taille de mémoire tampon raisonnable et à lire ou écrire dans une boucle.
    
> [!NOTE]
> COM possède une implémentation d'objet de stockage basée sur un tableau d'octets qui renvoie un objet **IEnumSTATSTG** à partir de la méthode **EnumElements** qui pose problème. En particulier, la méthode **QueryInterface** ne fonctionne pas correctement. Les fournisseurs de services qui implémentent leurs propres objets de stockage à l'aide de l'implémentation COM doivent créer un wrapper fin pour l'objet **IEnumSTATSTG** qui transfère les appels aux méthodes **IEnumSTATSTG** sous-jacentes, mais implémente son propre **AddRef **, Les méthodes **Release**, **QueryInterface**et **clone** . 
  

