---
title: Agissant comme un fournisseur de carnet d’adresse étrangère
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 6d532ed4-7dc5-46a9-995a-72bc97d16f6e
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: cafc6e3b6d863a7c2acec5811bf161ad0cd64458
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22570029"
---
# <a name="acting-as-a-foreign-address-book-provider"></a>Agissant comme un fournisseur de carnet d’adresse étrangère

**S’applique à**: Outlook 2013 | Outlook 2016 
  
Un fournisseur externe est un fournisseur de carnet d’adresses qui : 
  
- Attribue des identificateurs de modèle pour les destinataires.
    
- Prend en charge la méthode [IABLogon::OpenTemplateID](iablogon-opentemplateid.md) . 
    
- Fournit du code pour gérer les destinataires qui existent dans les conteneurs d’autres fournisseurs de carnet d’adresses appelés fournisseurs d’hébergement. Ce code comprend un objet property, généralement un **IMAPIProp** implémentation d’interface, qui inclut un objet property à partir du fournisseur d’hébergement. 
    
Comme un fournisseur externe est un rôle facultatif ; tous les fournisseurs doivent prendre en charge les identificateurs de modèle et leur code associé. Implémenter votre fournisseur en tant qu’un fournisseur externe si vous souhaitez contrôler les destinataires à l’aide de modèles fournis par votre fournisseur de créent des fournisseurs d’hébergement. 
  
Le format de votre fournisseur utilise pour les identificateurs d’entrée peut également servir pour les identificateurs de son modèle. Identificateurs de modèle doivent inclure inscrit votre fournisseur **MAPIUID** pour activer le protocole MAPI lier correctement destinataires pour les fournisseurs appropriés. 
  
Méthode de **IABLogon::OpenTemplateID** de votre fournisseur lorsqu’un appel de fournisseur d’hébergement [IMAPISupport::OpenTemplateID](imapisupport-opentemplateid.md)appels MAPI. Le fournisseur d’hébergement transmet l’identificateur du modèle du destinataire dans le paramètre _lpTemplateID_ dans son appel à **IMAPISupport::OpenTemplateID**. MAPI détermine que l’identificateur de modèle appartient à votre fournisseur en correspondance [MAPIUID](mapiuid.md) dans l’identificateur de modèle avec l' **MAPIUID** que votre fournisseur enregistré au moment de l’ouverture de session. MAPI achemine ensuite l’appel du fournisseur d’hébergement pour votre fournisseur par le biais de la méthode **IABLogon::OpenTemplateID** . 
  
Le fournisseur d’hébergement transfère également un pointeur à son implémentation d’objet de propriété pour le destinataire dans le paramètre _lpMAPIPropData_ , un identificateur d’interface dans le paramètre _lpInterface_ qui correspond au type d’implémentation d’interface transmis dans _lpMAPIPropData_et un indicateur facultatif, FILL_ENTRY. Votre fournisseur est prévu pour retourner dans le paramètre _lppMAPIPropNew_ un pointeur vers une implémentation d’objet de propriété du type spécifié dans _lpInterface_. Le pointeur retourné peut être à l’objet renvoyé à la ligne de propriété implémentée par votre fournisseur ou à l’objet fourni par le fournisseur d’hébergement dans _lpMAPIPropData_. Votre fournisseur doit retourner un pointeur d’objet propriété encapsulé lorsque :
  
- Affichage de la table du destinataire contient les contrôles de zone de liste.
    
- L’adresse de messagerie du destinataire doit être assemblée à partir des données dans plusieurs contrôles de tableau d’affichage.
    
- Problèmes de votre fournisseur affichent les notifications de table.
    
L’indicateur FILL_ENTRY indique à votre fournisseur que le fournisseur d’hébergement requiert toutes les propriétés du destinataire à mettre à jour. Votre fournisseur est nécessaire pour répondre à cette demande.
  
Lorsqu’un fournisseur d’hébergement appelle la méthode **OpenTemplateID** de votre fournisseur, votre fournisseur peut : 
  
- Mettre régulièrement à jour les données d’une entrée copiée.
    
- Conserver une entrée copiée synchronisée avec l’original, par exemple lorsqu’une entrée de carnet d’adresses est copiée dans le carnet d’adresses personnel.
    
- Implémentent des fonctionnalités qui ne peuvent pas être implémentées par le fournisseur de l’hôte, telles que le remplissage dynamique la liste des zones de tableau de détails de l’entrée copié à partir des données sur un serveur.
    
- Contrôler l’interaction entre les propriétés dans une entrée copiée ou le modèle instancié. Par exemple, informatique **ADRESSE_EMAIL_PR** à partir d’autres propriétés affichées dans la table Détails. 
    
Les deux premiers éléments sont des exemples de tâches qui ne nécessitent pas de votre fournisseur d’un objet property encapsulé — une implémentation **IMAPIProp** qui repose sur l’implémentation du fournisseur de l’hôte. Votre fournisseur peut mettre simplement à jour les propriétés en tant que nécessaire et de retour, le paramètre _lppMAPIPropNew_ pour pointer vers le pointeur passé par le fournisseur d’hébergement dans le paramètre _lpMAPIPropData_ . 
  
Les deux tâches requièrent que votre fournisseur retourne vers le fournisseur d’hébergement à un objet qui encapsule l’objet du fournisseur de l’hôte avec des fonctionnalités supplémentaires, telles que la possibilité d’afficher une feuille de propriétés de l’entrée. Cet objet peut être soit une messagerie utilisateur ou liste de distribution, selon le type d’objet passé par le fournisseur d’hébergement dans le paramètre _lpMAPIPropData_ et indiquée par l’identificateur d’interface dans le paramètre _lpInterface_ . Si le paramètre _lpMAPIPropData_ pointe vers un utilisateur de messagerie, votre objet de fournisseur de propriété renvoyé à la ligne doit être une implémentation **IMailUser** . Si _lpMAPIPropData_ pointe vers une liste de distribution, il doit être une implémentation **IDistList** . 
  
Objet encapsulé de votre fournisseur intercepte les appels de méthode **IMAPIProp** pour manipuler des spécifique au contexte du destinataire du fournisseur d’hébergement, l’objet, il est renvoyé. MAPI ne comporte qu’une condition requise pour les objets justifiés propriété : tous les appels vers [IMAPIProp::OpenProperty](imapiprop-openproperty.md) demande la propriété **PR_DETAILS_TABLE** ([PidTagDetailsTable](pidtagdetailstable-canonical-property.md)) doivent être passés au fournisseur d’hébergement. Implémentation de votre fournisseur peut utiliser la table renvoyée intercept afficher les notifications de table ou d’ajouter ses propres si nécessaire. 
  
La liste suivante présente les tâches qui sont généralement implémentées dans l’objet propriété encapsulé implémenté par les fournisseurs étrangères :
  
- Prétraitement et post-traitement des valeurs de propriété pour le destinataire de l’hôte dans [IMAPIProp::GetProps](imapiprop-getprops.md).
    
- Détails de la gestion d’affichent des contrôles de table, tels que les boutons et zones de liste dans **IMAPIProp::OpenProperty**.
    
- Validation ou la manipulation des valeurs de propriété pour le destinataire de l’hôte dans [IMAPIProp::SetProps](imapiprop-setprops.md).
    
- Informatique sociale propriétés requises, telles que **ADRESSE_EMAIL_PR** et vérifier que toutes les propriétés nécessaires ont été définies avant d’enregistrer le destinataire de l’hôte dans [IMAPIProp::SaveChanges](imapiprop-savechanges.md).
    
### <a name="to-implement-iablogonopentemplateid"></a>Pour mettre en œuvre IABLogon::OpenTemplateID
  
1. Vérifiez si l’identificateur de modèle passé avec le paramètre _lpTemplateID_ est valide et est dans un format reconnu par votre fournisseur. S’il n’est pas le cas, échouer et retourner MAPI_E_INVALID_ENTRYID. 
    
2. Créer un objet du type indiqué par l’identificateur de modèle, un utilisateur de messagerie, une liste de distribution ou un destinataire unique. 
    
3. Appelez la méthode **IUnknown::AddRef** dans un objet property du fournisseur d’hébergement, qui est l’objet désigné par le paramètre _lpMAPIPropData_ . 
    
4. Si le paramètre _ulTemplateFlags_ est défini sur FILL_ENTRY : 
    
   1. Si le nouvel objet est une messagerie utilisateur ou liste de distribution :
      
      1. Récupérer toutes les propriétés du nouvel objet, éventuellement en appelant la méthode **IMAPIProp::GetProps** . 
          
      2. Appelez du fournisseur hébergement **IMAPIProp::SetProps** pour copier toutes les propriétés récupérées à l’objet de propriété du fournisseur d’hébergement. 
      
   2. Si le nouvel objet est un destinataire unique, appeler la méthode de **IMAPIProp::SetProps** du fournisseur d’hébergement pour définir les propriétés suivantes : 
      
      - **TYPEADR_PR** ([PidTagAddressType](pidtagaddresstype-canonical-property.md)) pour le type d’adresse gérés par votre fournisseur.
        
      - **PR\_TEMPLATEID** ([PidTagTemplateid](pidtagtemplateid-canonical-property.md)) à l’identificateur de modèle à partir des paramètres _lpTemplateID_ et _cbTemplateID_ . 
        
      - **PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md)) DT_MAILUSER ou DT_DISTLIST, selon le cas.
    
5. Définir le contenu du paramètre _lppMAPIPropNew_ pour pointer vers le nouvel objet de votre fournisseur ou de l’objet property passé avec le paramètre _lpMAPIPropData_ , selon que votre fournisseur détermine qu'un objet encapsulé est nécessaire. 
    
6. Si une erreur critique se produit, par exemple une défaillance du réseau ou d’une insuffisance de mémoire, renvoie la valeur d’erreur appropriés. Cette valeur doit obtenir propagée au client avec la structure [MAPIERROR](mapierror.md) approprié, une tâche effectuée par le fournisseur d’hébergement. 
    

