---
title: Stockage structuré dans MAPI
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 642a678b-4bf2-4246-85cb-c798de23e36f
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 462ee84d5e9acd26f80bae6516179f21651749be
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19787287"
---
# <a name="structured-storage-in-mapi"></a>Stockage structuré dans MAPI

  
  
**S’applique à**: Outlook 
  
Stockage structuré fait référence à l’organisation hiérarchique de stockage introduit avec COM. Dans un environnement de stockage structuré, le stockage est divisé en deux ou trois types d’objets : 
  
- Objets Stream
    
- Verrouiller les objets octets
    
- Objets de stockage
    
Flux et verrouiller octets sont des objets de niveau inférieur qui accéder directement aux données. Objets Stream implémentent l’interface **IStream** qui définit des méthodes pour la lecture, écriture, de positionnement et la copie des octets de données. Verrouiller les objets octets implémentent une autre interface COM, **ILockBytes**, pour accéder aux données avec un tableau d’octets. Les tableaux d’octets sont généralement utilisés pour fournir un accès personnalisé vers un stockage sous-jacent.
  
Objets de stockage sont basés sur les objets octets flux ou de verrou ; ils peuvent contenir une ou plusieurs de ces objets ainsi que d’autres objets de stockage. Objets de stockage implémentent l’interface **IStorage** qui définit des méthodes pour la création, d’accès et de gestion des objets imbriqués. 
  
Étant **IStream**, **ILockBytes**et **IStorage** interfaces COM plutôt que des interfaces MAPI, leurs méthodes renvoient des valeurs d’erreur COM plutôt que des valeurs MAPI. Clients et fournisseurs de services de l’appel de méthodes dans ces interfaces doivent utiliser la fonction API **MapStorageSCode** pour convertir ces valeurs en valeurs d’erreur MAPI. Pour plus d’informations, voir [MapStorageSCode](mapstoragescode.md).
  
Clients et fournisseurs de services d’utilisent le stockage structuré pour travailler avec les propriétés qui sont trop volumineux pour tenir à jour les méthodes **IMAPIProp** , chaîne généralement volumineux et propriétés binaires. Une des méthodes courantes que les clients ou fournisseurs de services y accéder est en spécifiant l’identificateur d’interface dans un appel à la méthode [IMAPIProp::OpenProperty](imapiprop-openproperty.md) **IStream** ou **IStorage** . Par exemple, les clients appeler **OpenProperty** avec **PR_ATTACH_DATA_BIN** , ainsi que la balise de propriété IID_IStream l’identificateur d’interface pour accéder à une pièce jointe binaire dans un message. 
  
Clients et fournisseurs de services peuvent implémentent leurs propres flux et du stockage des objets ou appeler des fonctions API mises en œuvre d’accès fourni par MAPI ou COM. Comme les implémentations fournies traiter la plupart des cas, les clients et les fournisseurs de services rarement doivent créer leurs propres. 
  
Lorsqu’un client appelle **OpenProperty** sur un objet MAPI pour accéder à une de ses propriétés via un objet de stockage, le fournisseur de services s’ouvre généralement l’objet de stockage en mode direct. Toutefois, il s’agit par défaut au lieu de comportement requis. Les clients doivent partent du principe que tous les objets de stockage ouvert ou créé par les fournisseurs de services sont traitées et nécessitent un appel à **IStorage::Commit**. Ils doivent également n’oubliez pas que les modifications apportées aux objets de stockage pas sera définitive jusqu'à ce qu’ils appellent **IMAPIProp::SaveChanges** après la dernière **Valider** pour enregistrer l’objet MAPI. Pour plus d’informations, voir [IMAPIProp::SaveChanges](imapiprop-savechanges.md).
  
MAPI et COM fournissent plusieurs fonctions de l’API pour définir ou accéder aux objets de stockage et de flux de données. Les fonctions couramment utilisées sont décrits dans le tableau suivant.
  
**Fonctions permettant d’accéder aux objets Stream et stockage**

|**Fonction**|**Description**|
|:-----|:-----|
|[HrIStorageFromStream](hristoragefromstream.md) <br/> |Crée un objet de stockage pour accéder à un objet d’octets de flux de données ou de verrou.  <br/> |
|[OpenIMsgOnIStg](openimsgonistg.md) <br/> |Crée un objet de message pour accéder à un objet de stockage.  <br/> |
|[OpenStreamOnFile](openstreamonfile.md) <br/> |Crée un objet stream pour accéder à un fichier.  <br/> |
|[WrapCompressedRTFStream](wrapcompressedrtfstream.md) <br/> |Crée un objet stream qui contient la version compressée ou non compressée d’un objet stream contenant le texte enrichi d’un message.  <br/> |
   
 **Pour récupérer les noms des flux de données dans un sous-stockage donné**
  
1. Appelez du sous-stockage **IStorage::EnumElements** pour obtenir une interface **IEnumSTATSTG** . 
    
2. Appelez **IEnumSTATSTG::Next** avec structures **STATSTG** autant à la fois que vous le pouvez. Si vous demandez 100 à la fois, **suivant** généralement renvoie S_FALSE avec le contenu de _pceltFetched_ défini sur le numéro qui ont été réellement récupérées. 
    
3. Recherchez les structures **STATSTG** signalés avec STGTY_STREAM. 
    
4. Le paramètre _pwcsName_ version. 
    
 **Pour créer un objet de stockage pour accéder à un objet octets flux ou de verrou existant**
  
- Les clients appeler [HrIStorageFromStream](hristoragefromstream.md). 
    
 **Pour créer un objet de message pour accéder à un objet de stockage existant**
  
- Clients et fournisseurs de services d’appel [OpenIMsgOnIStg](openimsgonistg.md). Les objets de message généralement créés par les fournisseurs de banque de messages en ce sens qu’il ne prend pas en charge toutes les diffère de l’objet de message qui est créé le [IMessage : IMAPIProp](imessageimapiprop.md) méthodes, telles que **IMessage::SubmitMessage**de l’interface. Un paramètre d’entrée facultatif à **OpenIMsgOnIStg** est une fonction de rappel qui est conforme au prototype [MSGCALLRELEASE](msgcallrelease.md) . Cette fonction est appelée par le nouvel objet de message lorsque le décompte de références du message est égal à zéro. Implémentation d’une fonction **MSGCALLRELEASE** peut être utile pour effectuer un traitement finale avant que le nouveau message est complètement supprimé. 
    
[OpenStreamOnFile](openstreamonfile.md) est couramment utilisée pour stocker les pièces jointes, car elle crée un flux qui lit et écrit dans un fichier. **OpenProperty** avec **PR_ATTACH_DATA_BIN** en tant que la balise de propriété crée un flux pour le stockage des données binaires de pièce jointe. 
  
 **Pour compresser ou décompresser un flux de données contenant le texte du message dans le Format de texte enrichi**
  
- Les clients appeler [WrapCompressedRTFStream](wrapcompressedrtfstream.md). **WrapCompressedRTFStream** crée un flux qui encapsule le flux au format RTF. Le flux de wrapper n’implémente pas toutes les méthodes **IStream** ; les méthodes suivantes sont exclues : **Seek**, **SetSize**, **Rétablir**, **LockRegion**, **UnlockRegion**, **jours fériés**et **Clone**. C’est parce que les objets stream créés par **WrapCompressedRTFStream** ne prennent pas charge **SetSize** ou **Stat**, il n’est pas un moyen facile à étendre ou récupérer leur taille. La meilleure stratégie consiste à choisir une taille de mémoire tampon raisonnable et lire ou écrire dans une boucle.
    
> [!NOTE]
> COM a une implémentation d’objet de stockage basée sur un tableau d’octets qui renvoie un objet **IEnumSTATSTG** à partir de la méthode **EnumElements** qui pose problème. En particulier, la méthode **QueryInterface** ne fonctionne pas correctement. Fournisseurs de services qui implémentent leurs propres objets de stockage à l’aide de l’implémentation COM doivent créer une fine pour l’objet **IEnumSTATSTG** qui transfère les appels sur les méthodes **IEnumSTATSTG** sous-jacentes, mais implémente ses propres **AddRef **, Méthodes **Clone** , **QueryInterface**et **release**. 
  

