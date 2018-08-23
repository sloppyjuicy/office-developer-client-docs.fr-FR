---
title: IABLogonOpenTemplateID
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IABLogon.OpenTemplateID
api_type:
- COM
ms.assetid: 751c36d3-c39e-4357-a60a-88685a378de0
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: a120fb1710bf2bd351d956e4d05eb0af346ef4c5
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22583385"
---
# <a name="iablogonopentemplateid"></a>IABLogon::OpenTemplateID

  
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
Ouvre une entrée du destinataire qui comporte des données qui résident dans un fournisseur de carnet d’adresses hôte.
  
```cpp
HRESULT OpenTemplateID(
  ULONG cbTemplateID,
  LPENTRYID lpTemplateID,
  ULONG ulTemplateFlags,
  LPMAPIPROP lpMAPIPropData,
  LPCIID lpInterface,
  LPMAPIPROP FAR * lppMAPIPropNew,
  LPMAPIPROP lpMAPIPropSibling
);
```

## <a name="parameters"></a>Paramètres

 _cbTemplateID_
  
> [in] Le nombre d’octets dans l’identificateur de modèle indiqué par le paramètre _lpTemplateID_ . 
    
 _lpTemplateID_
  
> [in] Pointeur vers l’identificateur du modèle, ou la propriété de **PR_TEMPLATEID** ([PidTagTemplateid](pidtagtemplateid-canonical-property.md)), de l’entrée de destinataire à ouvrir.
    
 _ulTemplateFlags_
  
> [in] Un masque binaire composé des indicateurs utilisés pour indiquer comment ouvrir l’entrée représentée par l’identificateur de modèle. Vous pouvez définir l’indicateur suivant :
    
FILL_ENTRY 
  
> Le fournisseur d’hébergement crée une nouvelle entrée dans le conteneur en fonction de l’entrée représentée par l’identificateur de modèle. La méthode **IABLogon::OpenTemplateID** doit exécuter spécifique d’initialisation de l’entrée du fournisseur de l’hôte à l’aide de la [IMAPIProp : IUnknown](imapipropiunknown.md) implémentation dans le paramètre _lpMAPIPropData_ ou retour **IMAPIProp personnalisé **implémentation dans le paramètre _lppMAPIPropNew_ de l’interface. 
    
 _lpMAPIPropData_
  
> [in] Un pointeur vers l’objet property du fournisseur d’hébergement et l’implémentation d’une interface dérivé **IMAPIProp**.
    
 _lpInterface_
  
> [in] Pointeur vers l’identificateur d’interface (IID) qui représente le type de pointeur de l’interface à retourner dans le paramètre _lppMAPIPropNew_ . Le passage de **null** renvoie la norme d’interface utilisateur, la messagerie [IMailUser : IMAPIProp](imailuserimapiprop.md).
    
 _lppMAPIPropNew_
  
> [out] Un pointeur vers l’objet de la propriété liée et une implémentation d’une interface dérivé **IMAPIProp**.
    
 _lpMAPIPropSibling_
  
> [out] Réservé ; doit être **null**.
    
## <a name="return-value"></a>Valeur renvoy�e

S_OK 
  
> Le code a été correctement lié à des données liées dans le fournisseur d’hébergement.
    
MAPI_E_NO_SUPPORT 
  
> L’objet ne prend pas en charge les ID de modèle.
    
MAPI_E_UNKNOWN_ENTRYID 
  
> L’identificateur de modèle passé dans le paramètre _lpTemplateID_ n’est pas reconnue par le fournisseur de carnet d’adresses. 
    
## <a name="remarks"></a>Remarques

La méthode **IABLogon::OpenTemplateID** est implémentée uniquement par les fournisseurs de carnet d’adresses qui doivent contrôler les copies de leurs données qui sont trouvent dans les conteneurs de fournisseurs d’hébergement. Fournisseurs qui implémentent **OpenTemplateID** sont appelés fournisseurs de carnet d’adresse étrangère. Fournisseurs d’hébergement appeler [IMAPISupport::OpenTemplateID](imapisupport-opentemplateid.md) pour créer une entrée copiée ou ouvrir l’entrée copiée et MAPI passe à l’appel de **IABLogon::OpenTemplateID**. **IABLogon::OpenTemplateID** ouvre l’entrée et lie le code qui le contrôle à des données dans le fournisseur d’hébergement. 
  
Au lieu d’utiliser un identificateur d’entrée, **IABLogon::OpenTemplateID** utilise une autre propriété, identificateur du modèle de l’entrée, **PR_TEMPLATEID**. Identificateurs de modèle doivent être pris en charge pour les écritures dont le code doit être lié à des données dans un fournisseur d’hébergement.
  
Certains exemples de lorsqu’un fournisseur de carnet d’adresses doit implémenter **IABLogon::OpenTemplateID** sont les suivantes : 
  
- Pour mettre à jour régulièrement les données d’une entrée copiée afin qu’il reste synchronisé avec l’original.
    
- Pour implémenter les fonctionnalités que le fournisseur d’hébergement ne peut pas implémenter, telles que le remplissage dynamique d’une liste qui s’affiche dans la table des détails de l’entrée de données sur un serveur.
    
- Pour contrôler l’interaction entre les propriétés de l’entrée du fournisseur d’hébergement et l’entrée d’origine, telles que l’informatique **ADRESSE_EMAIL_PR** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md)) à partir des valeurs des contrôles modifier dans l’affichage des détails qui contiennent des différentes composants de l’adresse.
    
## <a name="notes-to-implementers"></a>Remarques destinées aux responsables de l’implémentation

Lorsqu’un fournisseur d’hébergement copie ou crée une entrée de votre fournisseur et que vous fournissez une implémentation d’objet de propriété via **IABLogon::OpenTemplateID**, vous gérez la plupart des appels à mettre à jour de l’entrée. Toutefois, car il est le fournisseur d’hébergement pour transférer les appels vers vous, le fournisseur d’hébergement peut intercepter des appels et exécuter le traitement personnalisé avant de transférer l’appel.
  
Vous devez utiliser les instructions suivantes votre propriété implémentations d’objets :
  
- Lorsque [IMAPIProp::GetProps](imapiprop-getprops.md) est appelé, déterminez si la demande est une propriété calculée et, s’il s’agit, gérer. Transférer toutes les demandes pour les propriétés non calculées pour le fournisseur d’hébergement. 
    
- Lorsque [IMAPIProp::OpenProperty](imapiprop-openproperty.md) est appelée pour ouvrir une table à l’exception des détails afficher le tableau, traiter la demande. La plupart des tables ne peut pas être copié avec précision pour le fournisseur d’hébergement. Vous devez générer l’implémentation **IMAPITable** pour ces tables demandés. La propriété **PR_DETAILS_TABLE** ([PidTagDetailsTable](pidtagdetailstable-canonical-property.md)) du tableau Détails doit être copiée vers le fournisseur d’hébergement. Cela permet à ce fournisseur générer la table localement. Vous voudrez peut-être enveloppe l’implémentation de table complet pour générer des notifications d’affichage tableau. 
    
- Lorsque [IMAPIProp::SetProps](imapiprop-setprops.md) est appelé, le fournisseur d’hébergement peut valider les données avant de vous permettant de définir les propriétés. Vous pouvez vérifier que toutes les propriétés nécessaires ont été définies ou calculées. Si une erreur est détectée, retourne la valeur d’erreur approprié et, si possible, des explications supplémentaires par le biais de [IMAPIProp::GetLastError](imapiprop-getlasterror.md).
    
- Lorsque [IMAPIProp::SaveChanges](imapiprop-savechanges.md) est appelé, le fournisseur d’hébergement souhaiterez peut-être effectuer un traitement avant d’enregistrer l’entrée. Vous devez enregistrer toutes les données qui sont affectées par les propriétés modifiées, par exemple une nouvelle adresse, dans l’entrée du fournisseur d’hébergement. 
    
En général, rendre votre implémentation de l’entrée que vous passez au fournisseur hôte intercepter toutes les méthodes pour manipuler des contextuelle des propriétés pertinentes. Si l’indicateur FILL_ENTRY est passé dans le paramètre _ulTemplateFlags_ , définissez toutes les propriétés de l’entrée. 
  
Si vous renvoyez un nouvel objet property dans le paramètre _lppMAPIPropNew_ , appeler la méthode [IUnknown::AddRef](http://msdn.microsoft.com/en-us/library/ms691379%28VS.85%29.aspx) d’objet de propriété du fournisseur d’hébergement de maintenir une référence. Une fois qu’ils sont traités par l’objet lié, tous les appels par le biais de l’objet lié l’implémentation **IMAPIProp** renvoyée dans _lppMAPIPropNew_ doivent être acheminés vers leur méthode correspondante dans l’objet de la propriété hôte. 
  
Les identificateurs de propriété de toute propriété nommée qui est transmise par le biais de l’objet de la propriété liée se trouvent dans l’espace de noms de votre fournisseur identificateur. Votre implémentation de la méthode [IMAPIProp::GetNamesFromIDs](imapiprop-getnamesfromids.md) doit déterminer les noms des propriétés afin qu’elle puisse exécuter des tâches spécifiques d’un modèle. De même, les propriétés votre fournisseur transmet au fournisseur hôte doivent également être dans votre espace de noms. Par exemple, si vous définissez une propriété nommée dans **OpenTemplateID**, vous devez utiliser un des identificateurs de votre pour le nom — sa création, le cas échéant, en appelant la méthode [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) . 
  
Si vous ne connaissez pas l’identificateur d’entrée passé _lpTemplateID_, retourne MAPI_E_UNKNOWN_ENTRYID.
  
Pour plus d’informations sur l’utilisation des identificateurs de modèle carnet d’adresse, voir [agissant comme un fournisseur de carnet d’adresses étrangère](acting-as-a-foreign-address-book-provider.md).
  
## <a name="see-also"></a>Voir aussi



[IMAPISupport::OpenTemplateID](imapisupport-opentemplateid.md)
  
[IPropData : IMAPIProp](ipropdataimapiprop.md)
  
[Propriété canonique PidTagTemplateid](pidtagtemplateid-canonical-property.md)
  
[IABLogon : IUnknown](iablogoniunknown.md)

