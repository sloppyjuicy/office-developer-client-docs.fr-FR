---
title: IMessageModifyRecipients
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMessage.ModifyRecipients
api_type:
- COM
ms.assetid: 2625f29d-325f-417d-bcec-49d580f9cd7e
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 3edcef69880dbc2a566a44582113c43802a47324
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19784141"
---
# <a name="imessagemodifyrecipients"></a>IMessage::ModifyRecipients

  
  
**S’applique à**: Outlook 
  
Ajoute, supprime ou modifie des destinataires du message.
  
```cpp
HRESULT ModifyRecipients(
  ULONG ulFlags,
  LPADRLIST lpMods
);
```

## <a name="parameters"></a>Param�tres

 _ulFlags_
  
> [in] Masque de bits d'indicateurs qui contr�le les modifications apport�es par destinataire. Si la valeur z�ro est transmise au param�tre  _ulFlags_, **ModifyRecipients** remplace tous les destinataires existantes avec la liste des destinataires d�sign�e par le param�tre  _lpMods_. Les indicateurs suivants peuvent �tre d�finis pour  _ulFlags_:
    
MODRECIP_ADD 
  
> Les destinataires d�sign�s par le param�tre  _lpMods_ doivent �tre ajout�es � la liste des destinataires. 
    
MODRECIP_MODIFY 
  
> Les destinataires d�sign�s par le param�tre  _lpMods_ doivent remplacer les destinataires existants. Toutes les propri�t�s existantes sont remplac�es par celles de la structure [ADRENTRY](adrentry.md) correspondante. 
    
MODRECIP_REMOVE 
  
> Destinataires existants doivent être retirés de la liste des destinataires à l’aide sous forme d’index de la propriété **PR_ROWID** ([PidTagRowid](pidtagrowid-canonical-property.md)) incluse dans le tableau de valeurs de propriété de chaque entrée du destinataire dans le paramètre _lpMods_ . 
    
 _lpMods_
  
> [in] Pointeur vers une structure [ADRLIST](adrlist.md) qui contient une liste de destinataires pour �tre ajout�s, supprim�s ou modifi�s dans le message. 
    
## <a name="return-value"></a>Valeur renvoy�e

S_OK 
  
> La liste des destinataires a �t� modifi�e avec succ�s.
    
## <a name="remarks"></a>Remarques

La m�thode **IMessage::ModifyRecipients** modifie la liste des destinataires du message. Il est � partir de cette liste, organis�e dans une structure [ADRLIST](adrlist.md) , que la table de destinataires est g�n�r�e. 
  
La structure **ADRLIST** contient une structure [ADRENTRY](adrentry.md) pour chaque destinataire et chaque structure **ADRENTRY** contient un tableau de valeurs de propri�t�s d�crivant les propri�t�s du destinataire. 
  
Destinataires de la structure **ADRLIST** peuvent �tre r�solus ou non r�solues. La diff�rence r�side dans le nombre et le type des propri�t�s qui sont inclus. Un destinataire non résolu contienne uniquement les **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) et les propriétés de **PR_RECIPIENT_TYPE** ([PidTagRecipientType](pidtagrecipienttype-canonical-property.md)) pendant un destinataire résolu contient ces deux propriétés ainsi que **TYPEADR_PR **([PidTagAddressType](pidtagaddresstype-canonical-property.md)) et **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)). Si **ADRESSE_EMAIL_PR** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md)) est disponible, il peut être inclus également.
  
Au moment o� qu'un message est envoy�, il doit inclure uniquement les destinataires r�solus dans sa liste des destinataires. Destinataires non r�solus provoquent des rapports de non-remise � �tre cr�� et envoy� � l'exp�diteur d'origine du message. Pour plus d'informations sur le processus de r�solution de nom � partir du point de vue du client, consultez la rubrique [r�solution d'un nom](resolving-a-recipient-name.md). Pour plus d'informations � partir du point de vue du fournisseur de carnet d'adresses, voir [Impl�mentation de la r�solution de noms](implementing-name-resolution.md).
  
En plus des destinataires r�solus et non r�solus, un destinataire peut �tre NULL. Le membre **cValues** de la structure **ADRENTRY** pour le destinataire est d�fini sur z�ro et le membre **rgPropVals** est d�fini sur NULL. 
  
## <a name="notes-to-callers"></a>Notes aux appelants

Vous pouvez cr�er une liste de destinataires en appelant [IAddrBook::Address](imapisupport-address.md) pour afficher la bo�te de dialogue commune et demandez � l'utilisateur de s�lectionner des entr�es. La liste d'adresses d�sign�e par le param�tre  _lppAdrList_ pour **Address** peut �tre transmise aux **ModifyRecipients** en tant que param�tre  _lpMods_. 
  
Lorsque vous sp�cifiez les propri�t�s d'un destinataire dans la structure [ADRLIST](adrlist.md) , inclure toutes les propri�t�s du destinataire, non seulement celles nouvelles ou modifi�es. Lorsqu'un destinataire est modifi�, toutes les propri�t�s non incluses dans la structure **ADRLIST** sont supprim�es. Pour r�cup�rer l'ensemble actuel des propri�t�s pour tous les destinataires d'un message, appelez [GetRecipientTable](imessage-getrecipienttable.md) et r�cup�rer toutes les lignes. Un **SRowSet** �tant identique en structure � une **ADRLIST**, vous pouvez les utiliser indiff�remment.
  
 **ModifyRecipients** remplace toutes les entr�es dans la liste des destinataires en cours avec les informations d�sign�es par  _lpMods_ lorsque aucun des indicateurs sont d�finies dans le param�tre  _ulFlags_. 
  
## <a name="notes-to-callers"></a>Notes aux appelants

Lorsque vous d�finissez l'indicateur MODRECIP_MODIFY, **ModifyRecipients** remplace chaque destinataire toute ligne par la ligne associ�e dans la structure [ADRLIST](adrlist.md) transmise dans  _lpMods_. Veillez � sp�cifier toutes les propri�t�s ayant un destinataire doit qu'elles ont chang� pour emp�cher leur involontairement supprim�.
  
Voici quelques r�gles pour d�finir les propri�t�s des destinataires dans la structure **ADRLIST**: 
  
- N'utilisez pas PT_NULL comme un type de propri�t�. **ModifyRecipients** renvoie une erreur si vous rencontrez cette valeur. 
    
- N'utilisez pas PT_ERROR comme un type de propri�t�. **ModifyRecipients** ignore cette valeur. 
    
- Inclure la propri�t� **PR_ROWID** pour tous les destinataires lorsque vous d�finissez l'indicateur MODRECIP_MODIFY ou MODRECIP_REMOVE dans  _ulFlags_. 
    
- N'incluez pas de la propri�t� **PR_ROWID** pour tous les destinataires lorsque vous d�finissez l'indicateur MODRECIP_ADD dans  _ulFlags_ ou lorsque vous transf�rez la valeur z�ro dans  _ulFlags_.
    
Si vous incluez soit la **PR_ADDRTYPE** propri�t� ou **PR_EMAIL_ADDRESS** pour un destinataire et un ou deux de ces propri�t�s sont incompatibles avec le type d'adresse et l'adresse du destinataire comme identifi� par **PR_ENTRYID**, les r�sultats ne sont pas d�finis. En d'autres termes, il existe trois possibilit�s, selon le fournisseur de services :
  
- Le message est remis � l'adresse d�crit par les propri�t�s **PR_ADDRTYPE** et **PR_EMAIL_ADDRESS**. 
    
- Le message est remis au destinataire identifi� par **PR_ENTRYID**.
    
- Le message sera d�clar� non remis en raison de l'ambigu�t� de l'adresse.
    
Utiliser les r�gles de r�partition d�crites dans la [Gestion de la m�moire ADRLIST et SRowSet des Structures](managing-memory-for-adrlist-and-srowset-structures.md) d'allocation de m�moire pour la liste des destinataires. **ModifyRecipients** ne la lib�re pas la structure **ADRLIST** ni aucun de ses sous-structures. La structure **ADRLIST** et chaque [SPropValue](spropvalue.md) doivent �tre allou�s s�par�ment � l'aide de la fonction [MAPIAllocateBuffer](mapiallocatebuffer.md) telle que chacun peut �tre lib�r� individuellement. Si la m�thode requiert un espace suppl�mentaire pour n'importe quelle structure **SPropValue**, elle peut remplacer la structure de **SPropValue** avec un fichier qui peut ult�rieurement lib�r� � l'aide de [MAPIFreeBuffer](mapifreebuffer.md). La structure **SPropValue** d'origine doit aussi �tre lib�r�e � l'aide de **MAPIFreeBuffer**.
  
## <a name="mfcmapi-reference"></a>Référence MFCMAPI

Pour des exemples de code MFCMAPI, voir le tableau suivant.
  
|**Fichier**|**Fonction**|**Commentaire**|
|:-----|:-----|:-----|
|MAPIABFunctions.cpp  <br/> |Ajouter destinataire  <br/> |MFCMAPI utilise la m�thode **IMessage::ModifyRecipients** pour ajouter un destinataire � un message.  <br/> |
   
## <a name="see-also"></a>Voir aussi



[ADRENTRY](adrentry.md)
  
[ADRLIST](adrlist.md)
  
[IAddrBook::Address](iaddrbook-address.md)
  
[IMAPISupport::Address](imapisupport-address.md)
  
[MAPIAllocateBuffer](mapiallocatebuffer.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[SPropValue](spropvalue.md)
  
[IMessage : IMAPIProp](imessageimapiprop.md)


[MFCMAPI comme un exemple de Code](mfcmapi-as-a-code-sample.md)

