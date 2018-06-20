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
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 27a5978d85cf06a31f583b82cd39d0001852876b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19784931"
---
# <a name="openimsgonistg"></a>OpenIMsgOnIStg

**S’applique à**: Outlook 
  
Crée un nouvel objet [IMessage](imessageimapiprop.md) par-dessus un objet OLE **IStorage** existant, à l’intérieur d’une session de messagerie. 
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |IMessage.h  <br/> |
|Implémentée par :  <br/> |MAPI  <br/> |
|Appelée par :  <br/> |Les applications clientes et des fournisseurs de services  <br/> |
   
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

## <a name="parameters"></a>Paramètres

_lpMsgSess_
  
> [in] Pointeur vers un objet de la session message dans laquelle nouvelle **IMessage**- sur - objet **IStorage** doit être créé. 
    
_lpAllocateBuffer_
  
> [in] Pointeur vers la fonction [MAPIAllocateBuffer](mapiallocatebuffer.md) , à utiliser pour allouer de la mémoire. 
    
_lpAllocateMore_
  
> [in] Pointeur vers la fonction [MAPIAllocateMore](mapiallocatemore.md) , à utiliser pour allouer plus de mémoire. 
    
_lpFreeBuffer_
  
> [in] Pointeur vers la fonction [MAPIFreeBuffer](mapifreebuffer.md) , à utiliser pour libérer de la mémoire. 
    
_lpMalloc_
  
> [in] Pointeur vers un objet d’allocation mémoire exposant l’interface OLE **IMalloc** . L’interface **IMessage** doit utiliser cette méthode de répartition lorsque vous travaillez avec des interfaces telles que **IStorage** et **IStream**. 
    
_lpMapiSup_
  
> [in] Facultatif pointeur vers un objet de prise en charge MAPI un fournisseur de services peut utiliser pour appeler les méthodes de le [IMAPISupport : IUnknown](imapisupportiunknown.md) interface. 
    
_lpStg_
  
> [entrée, sortie] Pointeur vers un objet OLE **IStorage** qui est ouvert et est en lecture seule ou autorisation en lecture/écriture. Étant donné que **IMessage** ne prend pas en charge l’accès en écriture uniquement, **OpenIMsgOnIStg** n’accepte pas un objet de stockage ouvert en mode écriture seule. 
    
_lpfMsgCallRelease_
  
> [in] Pointeur facultatif à une fonction de rappel selon le prototype [MSGCALLRELEASE](msgcallrelease.md) MAPI, vous pouvez appeler après la dernière version de l' objet **IStorage** - sur - **IMessage**. 
    
_ulCallerData_
  
> [in] Données de l’appelant enregistré par MAPI avec l’objet **IStorage** **IMessage**- sur - et transmises à la **MSGCALLRELEASE** en fonction de fonction de rappel. Les données fournissent le contexte sur l’objet **IMessage** libérée et l’objet **IStorage** sur lequel il a été généré. 
    
_ulFlags_
  
> [in] Masque de bits d’indicateurs permet de contrôler si la méthode OLE **IStorage::Commit** est appelée lorsque l’application cliente ou un fournisseur de services appelle la méthode **IMessage::SaveChanges** . Les indicateurs suivants peuvent être définis : 
    
IMSG_NO_ISTG_COMMIT 
  
> La méthode OLE **IStorage::Commit** ne pas doit être appelée lorsque le client ou le fournisseur appelle [SaveChanges](imapiprop-savechanges.md). 
    
MAPI_UNICODE
  
> Permet la création de fichiers de .msg Unicode. Le fichier [IMessage](imessageimapiprop.md) affiche STORE_UNICODE_OK dans son [PR_STORE_SUPPORT_MASK](pidtagstoresupportmask-canonical-property.md) et prend en charge les propriétés Unicode. 
    
  > [!NOTE]
  > L’indicateur MAPI_UNICODE est uniquement pris en charge dans cette fonction sur Outlook 2003 ou version ultérieure. 
  
_lppMsg_
  
> [out] Pointeur vers un pointeur vers l’objet **IMessage** ouvert. 
    
## <a name="return-value"></a>Valeur renvoy�e

S_OK 
  
> L'appel a r�ussi et a renvoy� la valeur attendue ou les valeurs.
    
## <a name="remarks"></a>Remarques

Attributs de la propriété est accessible uniquement sur propriété objets, autrement dit, l’implémentation de la [IMAPIProp : IUnknown](imapipropiunknown.md) interface. Pour rendre les propriétés MAPI disponible sur un objet de stockage structuré OLE, **OpenIMsgOnIStg** génère une [IMessage : IMAPIProp](imessageimapiprop.md) objet en haut de l’objet OLE **IStorage** . Les attributs de propriété sur de tels objets peuvent définir ou a été modifiés avec [SetAttribIMsgOnIStg](setattribimsgonistg.md) et récupérés par [GetAttribIMsgOnIStg](getattribimsgonistg.md). 
  
## <a name="notes-to-callers"></a>Notes aux appelants

Une session de messagerie doit être ouvert avec [OpenIMsgSession](openimsgsession.md) avant l’appel de **OpenIMsgOnIStg** . Fournissant un paramètre valide _lpMsgSess_ se sures que le nouveau message est créé au sein d’une session de messagerie afin qu’il est fermé lorsque la session est fermée. Si _lpMsgSess_ est NULL, le message est créé indépendamment de toute session de messagerie. Si l’application cliente ou un fournisseur de services qui a créé le message ne pas version il, ainsi que ses pièces jointes et ouvrir des tables, mémoire fuite et peut provoquer l’arrêt de l’application. 
  
MAPI utilise les fonctions désignées par _lpAllocateBuffer_, _lpAllocateMore_et _lpFreeBuffer_ pour la plupart de l’allocation de mémoire et de désaffectation, en particulier pour allouer de la mémoire pour une utilisation par les applications clientes lors de l’appel des interfaces de l’objet par exemple [IMAPIProp::GetProps](imapiprop-getprops.md) et [IMAPITable::QueryRows](imapitable-queryrows.md). Les pointeurs _lpAllocateBuffer_, _lpAllocateMore_et _lpFreeBuffer_ sont facultatifs lorsque la fonction **OpenIMsgOnIStg** est appelée avec un paramètre valide _lpMapiSup_ . 
  
Car elle porte sur un objet OLE sous-jacent, MAPI doit également utiliser l’allocation de mémoire OLE. Pour plus d’informations sur les objets de stockage structuré OLE et l’allocation de mémoire OLE, consultez la _référence du programmeur OLE_. 
  
Si une valeur valide est fournie pour _lpMapiSup_, **IMessage** prend en charge les indicateurs MAPI_DIALOG et ATTACH_DIALOG en appelant la méthode [IMAPISupport::DoProgressDialog](imapisupport-doprogressdialog.md) pour fournir une interface utilisateur d’avancement de [IMAPIProp::CopyTo](imapiprop-copyto.md) et les méthodes [IMessage::DeleteAttach](imessage-deleteattach.md) . En outre, la méthode [IMessage::ModifyRecipients](imessage-modifyrecipients.md) tente de convertir les identificateurs d’entrée à court terme pour les identificateurs d’entrée à long terme en appelant la méthode [IMAPISupport::OpenAddressBook](imapisupport-openaddressbook.md) et effectuer des appels sur l’objet de carnet d’adresses qui en résulte. Si la valeur NULL est passée pour _lpMapiSup_, **IMessage** ignore MAPI_DIALOG et ATTACH_DIALOG et stocke les identificateurs d’entrée à court terme sans conversion. 
  
L’objet **IStorage** désigné par le paramètre _lpStg_ doit être ouvert en mode STGM_READWRITE ou STGM_READ. Si le mode STGM_READWRITE est utilisé, le mode STGM_TRANSACTED doit également être défini. 
  
La fonction de rappel vers laquelle pointée le paramètre _lpfMsgCallRelease_ est facultative ; s’il est fourni, il doit être basé sur le prototype de fonction [MSGCALLRELEASE](msgcallrelease.md) . L’interface **IMessage** appelle lorsque le décompte de références de l’objet **IStorage** **IMessage**- sur - a la valeur zéro par le dernier appel à la méthode **Release** . La fonction de rappel est fréquemment utilisée pour libérer de l’interface **IStorage** sous-jacent. **IMessage** ne tente pas accéder à l’objet **IStorage** désigné par le paramètre _lpStg_ après avoir effectué le rappel. 
  
Certains clients ou des fournisseurs peuvent écrire des données supplémentaires à l’objet **IStorage** au-delà quel **IMessage** lui-même écrit lorsque la méthode [SaveChanges](imapiprop-savechanges.md) est appelée. Le client ou le fournisseur peut utiliser l’indicateur IMSG_NO_ISTG_COMMIT pour empêcher l’appel à la méthode OLE **IStorage::Commit** lors du traitement d’un appel de **SaveChanges** ; **IMessage** Dans ce cas le client ou le fournisseur doit lui-même valider l’objet **IStorage** lors de l’écriture de données supplémentaires. Pour faciliter cela, l’implémentation **IMessage** garantit nommer tous les substorages qu’il crée dans l’objet **IStorage** commençant par la chaîne « __ », autrement dit, avec deux traits de soulignement. Le client ou le fournisseur pour éviter les collisions de noms, en conservant les noms sous-stockage en dehors de cet espace de noms. 
  
MAPI ne définit pas le comportement de plusieurs opérations d’ouverture exécutée sur un sous-objet d’un message, comme une pièce jointe, un flux de données ou un message incorporé. MAPI permet actuellement un sous-objet qui est déjà ouvert à ouvrir une fois encore, mais MAPI effectue l’opération d’ouverture en incrémentant le décompte de références pour l’objet ouvert existant avant des retourner au client ou au fournisseur qui a appelé la [IMessage::OpenAttach ](imessage-openattach.md)ou la méthode [IMAPIProp::OpenProperty](imapiprop-openproperty.md) . Cela signifie que l’accès demandé pour la première opération open sur un sous-objet est l’accès fourni pour toutes les opérations open suivantes, quel que soit l’accès demandé par les opérations. 
  
La procédure correcte pour placer un message dans une pièce jointe est d’appeler la méthode [IMAPIProp::OpenProperty](imapiprop-openproperty.md) avec un identificateur d’interface de IID_IMessage. **OpenProperty** actuellement prend également en charge la création de pièces jointes des messages disponibles directement sur l’interface OLE **IStorage** , autrement dit, à l’aide de l’identificateur d’interface IID_IStorage. **IStorage** access est pris en charge pour autoriser un moyen facile placer un document Microsoft Word en pièce jointe sans le convertir vers ou à partir de l’interface OLE **IStream** . Toutefois, **IMessage** peut se comporter prévisible si **OpenIMsgOnIStg** est passé un pointeur **IStorage** pour les données de pièce jointe et les objets sont distribuées dans le bon ordre. 
  
## <a name="mfcmapi-reference"></a>Référence MFCMAPI

Pour des exemples de code MFCMAPI, voir le tableau suivant.
  
|**Fichier**|**Fonction**|**Commentaire**|
|:-----|:-----|:-----|
|File.cpp  <br/> |LoadMSGToMessage  <br/> |MFCMAPI utilise la méthode **OpenIMsgOnIStg** pour ouvrir une interface IMessage au-dessus de la. MSG fichier afin que le fichier peut être manipulé avec l’interface MAPI.  <br/> |
   
## <a name="see-also"></a>Voir aussi

- [MFCMAPI comme un exemple de Code](mfcmapi-as-a-code-sample.md)

