---
title: Création d’une liste de distribution
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: b63a6024-910d-4569-a3b4-c3ebf0b32c3d
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: fbf5985bfd3b0b14bdb3a4c5f896caed70fa5dbc
ms.sourcegitcommit: 5969c693475e22a3f5a4fdde3473ecc33013b76f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/09/2022
ms.locfileid: "62463092"
---
# <a name="creating-a-distribution-list"></a>Création d’une liste de distribution

**S’applique à** : Outlook 2013 | Outlook 2016 
  
Les clients peuvent créer une liste de distribution directement dans un conteneur modifiable tel que le carnet d’adresses personnel.
  
**Pour créer une liste de distribution dans le PAB**
  
1. Créez un tableau de balises de propriétés de taille moyenne avec **une balise de PR_DEF_CREATE_DL** ([PidTagDefCreateDl](pidtagdefcreatedl-canonical-property.md)), comme suit :
    
   ```cpp
    SizedPropTagArray(1, tagaDefaultDL) =
    {
        1,
        {
            PR_DEF_CREATE_DL
        }
    };
   ```

2. [Appelez IAddrBook::GetPAB](iaddrbook-getpab.md) pour récupérer l’identificateur d’entrée du carnet d’identité. En cas d’erreur ou **si GetPAB** renvoie zéro ou NULL, ne continuez pas. 
    
   ```cpp
    LPENTRYID peidPAB = NULL;
    ULONG cbeidPAB = 0;
    lpIAddrBook->GetPAB(&cbeidPAB, &peidPAB);
   ```

3. [Appelez IAddrBook::OpenEntry](iaddrbook-openentry.md) pour ouvrir le carnet d’annuaires. Le  _paramètre de sortie ulObjType_ doit être MAPI_ABCONT. 
    
   ```cpp
    ULONG ulObjType = 0;
    LPABCONT lpPABCont = NULL;
    lpIAddrBook->OpenEntry(cbeidPAB, peidPAB,
                    NULL,
                    MAPI_MODIFY,
                    &ulObjType,
                    &lpPABCont);
   ```

4. Appelez la méthode [IMAPIProp::GetProps](imapiprop-getprops.md) du PAB pour récupérer la propriété PR_DEF_CREATE_DL, le modèle qu’il utilise pour créer une liste de distribution. 
    
   ```cpp
    lpPABCont->GetProps(0,
                tagaDefaultDL,
                &lpspvDefDLTpl);
    
   ```

5. Si **GetProps échoue** : 
    
   1. Appelez la méthode [IMAPIProp::OpenProperty](imapiprop-openproperty.md) du PAB pour ouvrir la propriété **PR_CREATE_TEMPLATES** ([PidTagCreateTemplates](pidtagcreatetemplates-canonical-property.md)) avec l’interface **IMAPITable** . 
      
   2. Créez une restriction de propriété pour rechercher la ligne dont la **PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md)) est égale à « MAPIPDL ». 
      
   3. [Appelez IMAPITable::FindRow](imapitable-findrow.md) pour localiser cette ligne. 
    
6. Enregistrez l’identificateur d’entrée renvoyé **par GetProps** **ou FindRow**.
    
   ```cpp
    peidDefDLTpl = lpspvDefDLTpl->Value.bin.pb;
    cbeidDefDLTpl = lpspvDefDLTpl->Value.bin.cb;
    
   ```

7. Appelez la méthode [IABContainer::CreateEntry](iabcontainer-createentry.md) du PAB pour créer une entrée à l’aide du modèle représenté par l’identificateur d’entrée enregistré. Ne supposez pas que l’objet renvoyé sera une liste de distribution plutôt qu’un utilisateur de messagerie lorsque cet appel sera distant. Notez que l CREATE_CHECK_DUP est passé dans le paramètre _ulFlags_ pour empêcher l’ajout de l’entrée deux fois. 
    
   ```cpp
    lpPABCont->CreateEntry(cbeidDefDLTpl,
                    peidDefDLTPL,
                    CREATE_CHECK_DUP_STRICT,
                    &lpNewPABEntry);
   ```

8. Appelez la méthode **IUnknown::QueryInterface** de la nouvelle entrée, en passant IID_IDistList comme identificateur d’interface, pour déterminer si l’entrée est une liste de distribution et prend en charge l’interface [IDistList : IMAPIContainer](idistlistimapicontainer.md) . Étant **donné que CreateEntry** renvoie un pointeur **IMAPIProp** plutôt que le pointeur **IMailUser** ou **IDistList** plus spécifique, vérifiez qu’un objet de liste de distribution a été créé. Si **QueryInterface réussit** , vous pouvez être sûr d’avoir créé une liste de distribution plutôt qu’un utilisateur de messagerie. 
    
9. Appelez la méthode [IMAPIProp::SetProps](imapiprop-setprops.md) de la liste de distribution pour définir son nom d’affichage et d’autres propriétés. 
    
10. Appelez la méthode [IABContainer::CreateEntry](iabcontainer-createentry.md) de la liste de distribution pour ajouter un ou plusieurs utilisateurs de messagerie. 
    
11. Appelez la méthode [IMAPIProp::SaveChanges](imapiprop-savechanges.md) de la liste de distribution lorsque vous êtes prêt à l’enregistrer. Pour récupérer l’identificateur d’entrée de la liste de distribution enregistrée, définissez l’indicateur KEEP_OPEN_READWRITE, puis appelez [IMAPIProp::GetProps](imapiprop-getprops.md) demandant la propriété **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)).
    
12. Publiez la nouvelle liste de distribution et le PAB en appelant leurs **méthodes IUnknown::Release** . 
    
13. Appelez [MAPIFreeBuffer pour](mapifreebuffer.md) libérer la mémoire de l’identificateur d’entrée du PAB et du tableau de balises de propriétés de taille. 
    

