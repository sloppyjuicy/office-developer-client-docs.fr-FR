---
title: Rôle du fournisseur de carnets d’adresses étranger
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 6d532ed4-7dc5-46a9-995a-72bc97d16f6e
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 300681bd585e9d534113404a82f43565f4e79bb4
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435739"
---
# <a name="acting-as-a-foreign-address-book-provider"></a>Rôle du fournisseur de carnets d’adresses étranger

**S’applique à** : Outlook 2013 | Outlook 2016 
  
Un fournisseur étranger est un fournisseur de carnet d’adresses qui : 
  
- Affecte des identificateurs de modèle pour ses destinataires.
    
- Prend en [charge la méthode IABLogon::OpenTemplateID.](iablogon-opentemplateid.md) 
    
- Fournit du code pour la maintenance des destinataires qui existent dans les conteneurs d’autres fournisseurs de carnets d’adresses appelés fournisseurs d’hôtes. Ce code implique un objet de propriété, généralement une implémentation d’interface **IMAPIProp,** qui encapsule un objet de propriété à partir du fournisseur hôte. 
    
Agir en tant que fournisseur étranger est un rôle facultatif . Tous les fournisseurs n’ont pas besoin de prendre en charge les identificateurs de modèle et leur code associé. Implémentez votre fournisseur en tant que fournisseur étranger si vous souhaitez conserver le contrôle sur les destinataires créés par les fournisseurs d’hôtes à l’aide de modèles fournis par votre fournisseur. 
  
Le format que votre fournisseur utilise pour ses identificateurs d’entrée peut également être utilisé pour ses identificateurs de modèle. Les identificateurs de modèle doivent inclure le **MAPIUID** enregistré de votre fournisseur pour permettre à MAPI de lier correctement les destinataires aux fournisseurs appropriés. 
  
MAPI appelle la méthode **IABLogon::OpenTemplateID** de votre fournisseur lorsqu’un fournisseur d’hôte appelle [IMAPISupport::OpenTemplateID](imapisupport-opentemplateid.md). Le fournisseur hôte transmet l’identificateur de modèle du destinataire dans le paramètre  _lpTemplateID_ dans son appel à **IMAPISupport::OpenTemplateID**. MAPI détermine que l’identificateur de modèle appartient à votre fournisseur en faisant correspondre le [MAPIUID](mapiuid.md) dans l’identificateur de modèle avec le **MAPIUID** que votre fournisseur a enregistré au moment de l’inscription. MAPI a ensuite transmis l’appel du fournisseur hôte à votre fournisseur via la méthode **IABLogon::OpenTemplateID.** 
  
Le fournisseur hôte passe également un pointeur vers son implémentation d’objet de propriété pour le destinataire dans le paramètre  _lpMAPIPropData,_ un identificateur d’interface dans le paramètre  _lpInterface_ qui correspond au type d’implémentation d’interface transmis dans  _lpMAPIPropData_ et un indicateur facultatif, FILL_ENTRY. Votre fournisseur est censé renvoyer dans le paramètre  _lppMAPIPropNew_ un pointeur vers une implémentation d’objet de propriété du type spécifié dans  _lpInterface_. Le pointeur renvoyé peut être soit vers l’objet de propriété wrapped implémenté par votre fournisseur, soit vers l’objet fourni par le fournisseur hôte dans  _lpMAPIPropData_. Votre fournisseur doit renvoyer un pointeur d’objet de propriété wrapped lorsque :
  
- Le tableau d’affichage du destinataire contient des contrôles de zone de liste.
    
- L’adresse e-mail du destinataire doit être assemblée à partir de données dans plusieurs contrôles de table d’affichage.
    
- Les problèmes de votre fournisseur affichent les notifications du tableau.
    
L FILL_ENTRY indique à votre fournisseur que le fournisseur d’hôte requiert la mise à jour de toutes les propriétés du destinataire. Votre fournisseur est tenu de répondre à cette demande.
  
Lorsqu’un fournisseur d’hôte appelle la méthode **OpenTemplateID** de votre fournisseur, votre fournisseur peut : 
  
- Mettez régulièrement à jour les données d’une entrée copiée.
    
- Conservez une entrée copiée synchronisée avec son original, par exemple lorsqu’une entrée de carnet d’adresses est copiée dans le carnet d’adresses personnel.
    
- Implémenter des fonctionnalités qui ne peuvent pas être implémentées par le fournisseur hôte, telles que le remplissage dynamique des zones de liste dans la table de détails de l’entrée copiée à partir de données sur un serveur.
    
- Contrôler l’interaction entre les propriétés d’une entrée copiée ou d’un modèle ins instantié. Par exemple, le calcul **PR_EMAIL_ADDRESS** à partir d’autres propriétés affichées dans le tableau de détails. 
    
Les deux premiers éléments sont des exemples de tâches qui n’exigent pas que votre fournisseur fournisse un objet de propriété wrapped : une implémentation **d’IMAPIProp** basée sur l’implémentation du fournisseur hôte. Votre fournisseur peut simplement mettre à jour les propriétés selon les besoins et les renvoyer, en paramétrez le paramètre _lppMAPIPropNew_ pour qu’il pointe vers le pointeur transmis par le fournisseur hôte dans le paramètre _lpMAPIPropData._ 
  
Les deux deuxièmes tâches nécessitent que votre fournisseur retourne au fournisseur hôte un objet de propriété qui encapsule l’objet du fournisseur hôte avec des fonctionnalités supplémentaires, telles que la possibilité d’afficher une feuille de propriétés pour l’entrée. Cet objet de propriété sera un utilisateur de messagerie ou une liste de distribution, selon le type d’objet transmis par le fournisseur hôte dans le paramètre _lpMAPIPropData_ et indiqué par l’identificateur d’interface dans le paramètre _lpInterface._ Si le _paramètre lpMAPIPropData_ pointe vers un utilisateur de messagerie, l’objet de propriété wrapped de votre fournisseur doit être une implémentation **IMailUser.** Si _lpMAPIPropData_ pointe vers une liste de distribution, il doit s’agit d’une **implémentation IDistList.** 
  
L’objet de propriété wrapped de votre fournisseur intercepte les appels de méthode **IMAPIProp** pour effectuer une manipulation spécifique du contexte du destinataire du fournisseur hôte (l’objet qu’il enveloppe). MAPI n’a qu’une seule condition requise pour les objets de propriété wrapped : tous les appels à [IMAPIProp::OpenProperty](imapiprop-openproperty.md) demandant la propriété **PR_DETAILS_TABLE** ([PidTagDetailsTable](pidtagdetailstable-canonical-property.md)) doivent être transmis au fournisseur d’hôte. L’implémentation de votre fournisseur peut utiliser le tableau renvoyé pour intercepter les notifications de la table d’affichage ou pour ajouter la vôtre si nécessaire. 
  
La liste suivante inclut les tâches qui sont généralement implémentées dans l’objet de propriété wrapped implémenté par des fournisseurs étrangers :
  
- Valeurs de propriété de prétraitage et de post-traitement pour le destinataire hôte dans [IMAPIProp::GetProps](imapiprop-getprops.md).
    
- La gestion des détails affiche les contrôles de tableau, tels que les boutons et les zones de liste, dans **IMAPIProp::OpenProperty**.
    
- Validation ou manipulation des valeurs de propriété pour le destinataire hôte dans [IMAPIProp::SetProps](imapiprop-setprops.md).
    
- Calcul des propriétés requises telles que **PR_EMAIL_ADDRESS** et vérification que toutes les propriétés nécessaires ont été définies avant d’enregistrer le destinataire hôte dans [IMAPIProp::SaveChanges](imapiprop-savechanges.md).
    
### <a name="to-implement-iablogonopentemplateid"></a>Pour implémenter IABLogon::OpenTemplateID
  
1. Vérifiez si l’identificateur de modèle transmis avec le paramètre  _lpTemplateID_ est valide et est dans un format reconnu par votre fournisseur. Si ce n’est pas le cas, échouez et renvoyez MAPI_E_INVALID_ENTRYID. 
    
2. Créez un objet du type indiqué par l’identificateur de modèle, soit un utilisateur de messagerie, une liste de distribution, soit un destinataire unique. 
    
3. Appelez **la méthode IUnknown::AddRef** dans l’objet de propriété du fournisseur hôte, qui est l’objet pointé par le paramètre _lpMAPIPropData._ 
    
4. Si le  _paramètre ulTemplateFlags_ est FILL_ENTRY : 
    
   1. Si le nouvel objet est un utilisateur de messagerie ou une liste de distribution :
      
      1. Récupérez toutes les propriétés du nouvel objet, éventuellement en appelant sa méthode **IMAPIProp::GetProps.** 
          
      2. Appelez la méthode **IMAPIProp::SetProps** du fournisseur hôte pour copier toutes les propriétés récupérées dans l’objet de propriété du fournisseur hôte. 
      
   2. Si le nouvel objet est un destinataire uniques, appelez la méthode **IMAPIProp::SetProps** du fournisseur hôte pour définir les propriétés suivantes : 
      
      - **PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md)) au type d’adresse géré par votre fournisseur.
        
      - **PR \_ TEMPLATEID** ([PidTagTemplateid](pidtagtemplateid-canonical-property.md)) vers l’identificateur de modèle à partir des paramètres _lpTemplateID_ et _cbTemplateID._ 
        
      - **PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md)) pour DT_MAILUSER ou DT_DISTLIST, le cas échéant.
    
5. Définissez le contenu du paramètre  _lppMAPIPropNew_ de façon à pointer vers le nouvel objet de votre fournisseur ou l’objet de propriété transmis avec le paramètre  _lpMAPIPropData,_ selon que votre fournisseur détermine si un objet wrapped est nécessaire. 
    
6. Si une erreur critique se produit, telle qu’une défaillance réseau ou une condition de mémoire insérable, renvoyez la valeur d’erreur appropriée. Cette valeur doit être propagée au client avec la structure [MAPIERROR](mapierror.md) appropriée, une tâche effectuée par le fournisseur d’hôtes. 
    

