---
title: Création d’une liste de distribution
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: b63a6024-910d-4569-a3b4-c3ebf0b32c3d
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: 82fa28f021dbb839c7bb05974682f0bb24174bb2
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19783098"
---
# <a name="creating-a-distribution-list"></a>Création d’une liste de distribution

**S’applique à**: Outlook 
  
Les clients peuvent créer une liste de distribution directement dans un conteneur modifiable telles que le carnet d’adresses personnel (CAP).
  
**Pour créer une liste de distribution dans le carnet d’adresses personnel**
  
1. Créez un tableau de balise de propriété ajustés avec la balise d’une propriété, **PR_DEF_CREATE_DL** ([PidTagDefCreateDl](pidtagdefcreatedl-canonical-property.md)), comme suit :
    
   ```cpp
    SizedPropTagArray(1, tagaDefaultDL) =
    {
        1,
        {
            PR_DEF_CREATE_DL
        }
    };
   ```

2. Appelez [IAddrBook::GetPAB](iaddrbook-getpab.md) pour récupérer l’identificateur d’entrée du carnet d’adresses personnel. Si une erreur se produit ou **GetPAB** renvoie zéro ou NULL, ne continuez pas. 
    
   ```cpp
    LPENTRYID peidPAB = NULL;
    ULONG cbeidPAB = 0;
    lpIAddrBook->GetPAB(&cbeidPAB, &peidPAB);
   ```

3. Appelez [IAddrBook::OpenEntry](iaddrbook-openentry.md) pour ouvrir le carnet d’adresses personnel. Le paramètre de sortie _ulObjType_ doit être défini sur MAPI_ABCONT. 
    
   ```cpp
    ULONG ulObjType = 0;
    LPABCONT lpPABCont = NULL;
    lpIAddrBook->OpenEntry(cbeidPAB, peidPAB,
                    NULL,
                    MAPI_MODIFY,
                    &ulObjType,
                    &lpPABCont);
   ```

4. Appeler [IMAPIProp::GetProps](imapiprop-getprops.md) méthode le carnet d’adresses du personnel pour récupérer la propriété PR_DEF_CREATE_DL, le modèle utilisé pour créer une liste de distribution. 
    
   ```cpp
    lpPABCont->GetProps(0,
                tagaDefaultDL,
                &lpspvDefDLTpl);
    
   ```

5. En cas d’échec de **GetProps** : 
    
   1. Appelez le carnet d’adresses du personnel [IMAPIProp::OpenProperty](imapiprop-openproperty.md) pour ouvrir la propriété **PR_CREATE_TEMPLATES** ([PidTagCreateTemplates](pidtagcreatetemplates-canonical-property.md)) avec l’interface **IMAPITable** . 
      
   2. Créer une restriction de propriété pour rechercher la ligne contenant la colonne **TYPEADR_PR** ([PidTagAddressType](pidtagaddresstype-canonical-property.md)) égale à « MAPIPDL ». 
      
   3. Appel [IMAPITable::FindRow](imapitable-findrow.md) pour rechercher cette ligne. 
    
6. Enregistrez l’identificateur d’entrée renvoyée par **GetProps** ou **FindRow**.
    
   ```cpp
    peidDefDLTpl = lpspvDefDLTpl->Value.bin.pb;
    cbeidDefDLTpl = lpspvDefDLTpl->Value.bin.cb;
    
   ```

7. Appelez le carnet d’adresses du personnel [IABContainer::CreateEntry](iabcontainer-createentry.md) pour créer une nouvelle entrée à l’aide du modèle représenté par l’identificateur d’entrée enregistrée. Ne pensez pas que l’objet retourné sera une liste de distribution plutôt que d’un utilisateur de messagerie lorsque cet appel est distant. Notez que l’indicateur CREATE_CHECK_DUP est passé dans le paramètre _ulFlags_ pour empêcher que l’entrée ajoutée à deux reprises. 
    
   ```cpp
    lpPABCont->CreateEntry(cbeidDefDLTpl,
                    peidDefDLTPL,
                    CREATE_CHECK_DUP_STRICT,
                    &lpNewPABEntry);
   ```

8. Appeler la méthode **IUnknown::QueryInterface** de la nouvelle entrée, en passant IID_IDistList comme l’identificateur d’interface pour déterminer si l’entrée est une liste de distribution et prend en charge la [IDistList : IMAPIContainer](idistlistimapicontainer.md) interface. **CreateEntry** renvoie un pointeur **IMAPIProp** plutôt que le pointeur **IMailUser** ou **IDistList** plus spécifique, vérifiez que l’objet d’une liste de distribution a été créé. Si **QueryInterface** réussit, vous pouvez être sûr que vous avez créé une liste de distribution plutôt que d’un utilisateur de messagerie. 
    
9. Appelez la méthode [IMAPIProp::SetProps](imapiprop-setprops.md) de la liste de distribution pour définir son nom d’affichage et d’autres propriétés. 
    
10. Appelez la méthode [IABContainer::CreateEntry](iabcontainer-createentry.md) de la liste de distribution pour ajouter un ou plusieurs utilisateurs de messagerie. 
    
11. Appelez la méthode [IMAPIProp::SaveChanges](imapiprop-savechanges.md) de la liste de distribution lorsque vous êtes prêt à enregistrer. Pour récupérer l’identificateur d’entrée de la liste de distribution enregistrée, définir l’indicateur KEEP_OPEN_READWRITE, puis appelez [IMAPIProp::GetProps](imapiprop-getprops.md) demande la propriété **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)).
    
12. Publier la nouvelle liste de distribution et le carnet d’adresses personnel en appelant leurs méthodes **IUnknown::Release** . 
    
13. Appelez [MAPIFreeBuffer](mapifreebuffer.md) pour libérer de la mémoire pour l’identificateur d’entrée du carnet d’adresses personnel et le tableau de balise de propriété ajustés. 
    

