---
title: OpenIMsgOnIStg
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- OpenIMsgOnIStg
api_type:
- HeaderDef
ms.assetid: a98b0b26-9b19-44ca-9b4e-0ad4d1c54325
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 6d5ed20e532f0893757cc46d9ea478c7b65acc86
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33406520"
---
# <a name="openimsgonistg"></a>OpenIMsgOnIStg

**S’applique à** : Outlook 2013 | Outlook 2016 
  
Crée un nouvel objet [IMessage](imessageimapiprop.md) au-dessus d’un objet OLE **IStorage** existant, à utiliser dans une session de message. 
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Imessage.h  <br/> |
|Implémenté par :  <br/> |MAPI  <br/> |
|Appelé par :  <br/> |Applications clientes et fournisseurs de services  <br/> |
   
```cpp
SCODE OpenIMsgOnIStg(
  LPMSGSESS lpMsgSess,
  LPALLOCATEBUFFER lpAllocateBuffer,
  LPALLOCATEMORE lpAllocateMore,
  LPFREEBUFFER lpFreeBuffer,
  LPMALLOC lpmalloc,
  LPVOID lpMapiSup,
  LPSTORAGE lpStg,
  MSGCALLRELEASE FAR * lpfMsgCallRelease,
  ULONG ulCallerData,
  ULONG ulFlags,
  LPMESSAGE FAR * lppMsg
);
```

## <a name="parameters"></a>Parameters

_lpMsgSess_
  
> [in] Pointeur vers un objet de session de message dans lequel le nouvel objet **IMessage**-on- **IStorage** doit être créé. 
    
_lpAllocateBuffer_
  
> [in] Pointeur vers la [fonction MAPIAllocateBuffer,](mapiallocatebuffer.md) à utiliser pour allouer de la mémoire. 
    
_lpAllocateMore_
  
> [in] Pointeur vers la [fonction MAPIAllocateMore,](mapiallocatemore.md) à utiliser pour allouer de la mémoire supplémentaire. 
    
_lpFreeBuffer_
  
> [in] Pointeur vers la [fonction MAPIFreeBuffer,](mapifreebuffer.md) à utiliser pour libérer de la mémoire. 
    
_lpMalloc_
  
> [in] Pointeur vers un objet d’allocation de mémoire exposant l’interface OLE **IMalloc.** **L’interface IMessage** doit utiliser cette méthode d’allocation lors de l’utilisation d’interfaces telles que **IStorage** **et IStream**. 
    
_lpMapiSup_
  
> [in] Pointeur facultatif vers un objet de support MAPI qu’un fournisseur de services peut utiliser pour appeler les méthodes de l’interface [IMAPISupport : IUnknown.](imapisupportiunknown.md) 
    
_lpStg_
  
> [in, out] Pointeur vers un objet **OLE IStorage** qui est ouvert et qui dispose d’une autorisation en lecture seule ou en lecture/écriture. Étant **donné que IMessage** ne prend pas en charge l’accès en écriture seule, **OpenIMsgOnIStg** n’accepte pas un objet de stockage ouvert en mode écriture seule. 
    
_lpfMsgCallRelease_
  
> [in] Pointeur facultatif vers une fonction de rappel basée sur le prototype [MSGCALLRELEASE](msgcallrelease.md) que MAPI doit appeler après la dernière version de l’objet **IMessage**-on- **IStorage.** 
    
_ulCallerData_
  
> [in] Données de l’appelant enregistrées par MAPI avec l’objet **IMessage**-on- **IStorage** et transmises à la fonction de rappel **MSGCALLRELEASE.** Les données fournissent un contexte sur l’objet **IMessage** en cours de libération et l’objet **IStorage** sur lequel il a été créé. 
    
_ulFlags_
  
> [in] Masque de bits d’indicateurs utilisés pour contrôler si la méthode OLE **IStorage::Commit** est appelée lorsque l’application cliente ou le fournisseur de services appelle la méthode **IMessage::SaveChanges.** Les indicateurs suivants peuvent être définies : 
    
IMSG_NO_ISTG_COMMIT 
  
> La méthode OLE **IStorage::Commit** ne doit pas être appelée lorsque le client ou le fournisseur appelle [SaveChanges](imapiprop-savechanges.md). 
    
MAPI_UNICODE
  
> Permet la création de fichiers .msg Unicode. Le fichier [IMessage](imessageimapiprop.md) qui en résulte affiche STORE_UNICODE_OK sa PR_STORE_SUPPORT_MASK [et](pidtagstoresupportmask-canonical-property.md) prend en charge les propriétés Unicode. 
    
  > [!NOTE]
  > L MAPI_UNICODE est uniquement pris en charge dans cette fonction sur Outlook 2003 ou supérieure. 
  
_lppMsg_
  
> [out] Pointeur vers un pointeur vers l’objet **IMessage** ouvert. 
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> L'appel a r�ussi et a renvoy� la valeur attendue ou les valeurs.
    
## <a name="remarks"></a>Remarques

Les attributs de propriété sont accessibles uniquement sur les objets de propriété, c’est-à-dire les objets implémentant l’interface [IMAPIProp : IUnknown.](imapipropiunknown.md) Pour rendre les propriétés MAPI disponibles sur un objet de stockage structuré OLE, **OpenIMsgOnIStg** crée un objet [IMessage : IMAPIProp](imessageimapiprop.md) au-dessus de l’objet **OLE IStorage.** Les attributs de propriété sur ces objets peuvent être définies ou modifiées avec [SetAttribIMsgOnIStg](setattribimsgonistg.md) et récupérées avec [GetAttribIMsgOnIStg](getattribimsgonistg.md). 
  
## <a name="notes-to-callers"></a>Remarques pour les appelants

Une session de message doit être ouverte avec [OpenIMsgSession](openimsgsession.md) avant l’appel **d’OpenIMsgOnIStg.** La fourniture d’un paramètre  _lpMsgSess_ valide permet de s’assurer que le nouveau message est créé au sein d’une session de message afin qu’il soit fermé à la fermeture de la session. Si  _lpMsgSess_ est NULL, le message est créé indépendamment de toute session de message. Si l’application cliente ou le fournisseur de services qui a créé le message ne le libère pas, ainsi que toutes ses pièces jointes et tables ouvertes, la mémoire est perdue et l’application peut s’interrompre. 
  
MAPI utilise les fonctions pointées par  _lpAllocateBuffer_,  _lpAllocateMore_ et  _lpFreeBuffer_ pour la plupart de l’allocation et de la déallocation de mémoire, en particulier pour allouer de la mémoire pour une utilisation par les applications clientes lors de l’appel d’interfaces d’objets telles que [IMAPIProp::GetProps](imapiprop-getprops.md) et [IMAPITable::QueryRows](imapitable-queryrows.md). Les pointeurs  _lpAllocateBuffer,_  _lpAllocateMore_ et  _lpFreeBuffer_ sont facultatifs lorsque la fonction **OpenIMsgOnIStg** est appelée avec un paramètre  _lpMapiSup_ valide. 
  
Étant donné qu’il traite un objet OLE sous-jacent, MAPI doit également utiliser l’allocation de mémoire OLE. Pour plus d’informations sur les objets de stockage structuré OLE et l’allocation de mémoire OLE, voir la référence du programmeur _OLE._ 
  
Si une valeur valide est fournie pour _lpMapiSup,_ **IMessage** prend en charge les indicateurs MAPI_DIALOG et ATTACH_DIALOG en appelant la méthode [IMAPISupport::D oProgressDialog](imapisupport-doprogressdialog.md) pour fournir une interface utilisateur de progression pour les méthodes [IMAPIProp::CopyTo](imapiprop-copyto.md) et [IMessage::D eleteAttach.](imessage-deleteattach.md) En outre, la méthode [IMessage::ModifyRecipients](imessage-modifyrecipients.md) tente de convertir des identificateurs d’entrée à court terme en identificateurs d’entrée à long terme en appelant la méthode [IMAPISupport::OpenAddressBook](imapisupport-openaddressbook.md) et en appelant l’objet carnet d’adresses résultant. Si NULL est transmis pour  _lpMapiSup,_ **IMessage** ignore les MAPI_DIALOG et ATTACH_DIALOG et stocke les identificateurs d’entrée à court terme sans conversion. 
  
**L’objet IStorage** pointé par le paramètre _lpStg_ doit être ouvert en mode STGM_READ ou STGM_READWRITE. Si le mode STGM_READWRITE est utilisé, le mode STGM_TRANSACTED doit également être définie. 
  
La fonction de rappel pointée par _le paramètre lpfMsgCallRelease_ est facultative ; s’il est fourni, il doit être basé sur le prototype de fonction [MSGCALLRELEASE.](msgcallrelease.md) **L’interface IMessage** l’appelle lorsque le nombre de références de l’objet **IMessage**-on- **IStorage** est définie sur zéro par le dernier appel de sa méthode **Release.** La fonction de rappel est couramment utilisée pour libérer l’interface **IStorage** sous-jacente. **IMessage** ne tente pas d’accéder à l’objet **IStorage** pointé par le paramètre  _lpStg_ après avoir fait le rappel. 
  
Certains clients ou fournisseurs peuvent écrire des données supplémentaires dans l’objet **IStorage** au-delà de ce **qu’IMessage** écrit lui-même lorsque sa méthode [SaveChanges](imapiprop-savechanges.md) est appelée. Le client ou le fournisseur peut utiliser l’indicateur IMSG_NO_ISTG_COMMIT pour empêcher **IMessage** d’appeler la méthode OLE **IStorage::Commit** lors du traitement d’un appel **SaveChanges** ; dans ce cas, le client ou le fournisseur doit valider lui-même l’objet **IStorage** lorsque les données supplémentaires sont écrites. Pour ce faire, l’implémentation **IMessage** garantit le nom de tous les sous-torages qu’elle crée dans l’objet **IStorage** en commençant par la chaîne « __ », c’est-à-dire avec deux traits de soulignement. Le client ou le fournisseur peut éviter les collisions de noms en maintenant les noms de ses sous-clients en dehors de cet espace de noms. 
  
MAPI ne définit pas le comportement de plusieurs opérations d’ouverture effectuées sur un sous-objet d’un message, comme une pièce jointe, un flux ou un message incorporé. MAPI autorise actuellement l’ouverture d’un sous-objet déjà ouvert, mais MAPI effectue l’opération d’ouverture en incrémentant le nombre de références pour l’objet ouvert existant et en le renvoyant au client ou au fournisseur qui a appelé la méthode [IMessage::OpenAttach](imessage-openattach.md) ou [IMAPIProp::OpenProperty.](imapiprop-openproperty.md) Cela signifie que l’accès demandé pour la première opération d’ouverture sur un sous-objet est l’accès fourni pour toutes les opérations d’ouverture suivantes, quel que soit l’accès demandé par les opérations. 
  
La procédure correcte pour placer un message dans une pièce jointe consiste à appeler la méthode [IMAPIProp::OpenProperty](imapiprop-openproperty.md) avec un identificateur d’interface IID_IMessage. **OpenProperty** prend actuellement en charge la création de pièces jointes de message disponibles directement sur l’interface OLE **IStorage,** c’est-à-dire, à l’aide de l’identificateur IID_IStorage’interface. **L’accès iStorage** est pris en charge pour permettre un moyen simple de placer un document Microsoft Word dans une pièce jointe sans le convertir vers ou à partir de l’interface OLE **IStream.** Toutefois, **IMessage** peut ne pas se comporter de manière prévisible si **OpenIMsgOnIStg** est transmis un pointeur **IStorage** aux données de pièce jointe, puis les objets sont libérés dans le mauvais ordre. 
  
## <a name="mfcmapi-reference"></a>Référence MFCMAPI

Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.
  
|**Fichier**|**Fonction**|**Commentaire**|
|:-----|:-----|:-----|
|File.cpp  <br/> |LoadMSGToMessage  <br/> |MFCMAPI utilise la **méthode OpenIMsgOnIStg** pour ouvrir une interface IMessage sur le . Fichier MSG afin que le fichier puisse être manipulé avec MAPI.  <br/> |
   
## <a name="see-also"></a>Voir aussi

- [MFCMAPI comme un exemple de Code](mfcmapi-as-a-code-sample.md)

