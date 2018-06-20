---
title: Implémentation d’objet état
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 48fd3e28-c2d2-474d-9487-5e2f08ca7319
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: 379378f2092f7b119a40ac44cbdcfa03f254b448
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19787265"
---
# <a name="status-object-implementation"></a>Implémentation d’objet état

**S’applique à**: Outlook 
  
Tous les fournisseurs de services doivent implémenter un objet d’état et fournir des propriétés à partir de celui-ci à la table d’état de session. Vous pouvez inclure une ou plusieurs lignes dans la table d’état, en fonction du nombre de ressources que vous contrôlez. Par exemple, un fournisseur de transport doit créer une ligne dans la table d’état pour chaque file d’attente de message qu’il gère. Lorsque des modifications se produisent, la ligne de tableau statut approprié doit être mis à jour. Objets d’état sont implémentées pour fournir l’accès à la fois pour les informations contenues dans la table d’état et des informations supplémentaires non inclus dans le tableau.
  
### <a name="to-implement-a-status-object"></a>Pour implémenter un objet d’état

1. Implémentez la méthode **OpenStatusEntry** de l’objet d’ouverture de session. Lorsque les clients souhaitent ouvrir votre objet état, ils appellent [IMAPISession::OpenEntry](imapisession-openentry.md). MAPI répond à la demande d’ouverture en appelant la méthode **OpenStatusEntry** de votre fournisseur, à l’origine de votre fournisseur ouvrir son objet état et revenir au client un pointeur vers son implémentation **IMAPIStatus** . Dans votre implémentation **OpenStatusEntry** , procédez comme suit : 
    
   1. Effectuer les tâches suivantes si votre objet de connexion n’a pas encore créé un objet d’état :
    
      1. Appeler la méthode [IMAPISupport::OpenProfileSection](imapisupport-openprofilesection.md) de l’objet de la prise en charge pour accéder à section de profil de votre fournisseur. 
          
      2. Créer un nouvel objet d’état.
          
      3. Stocker une référence à la section profil dans l’objet d’état de votre fournisseur et appeler la méthode [IUnknown::AddRef](http://msdn.microsoft.com/library/b4316efd-73d4-4995-b898-8025a316ba63%28Office.15%29.aspx) de la section profil pour incrémenter son décompte de références. 
          
      4. Stocker une référence à l’objet d’ouverture de session dans l’objet d’état de votre fournisseur et appelez la méthode **IUnknown::AddRef** de l’objet d’ouverture de session pour incrémenter son décompte de références. 
          
      5. Stocker une référence à l’objet de l’état de l’objet de connexion de votre fournisseur.
    
   2. Appeler la méthode **IUnknown::AddRef** de l’objet état pour incrémenter son décompte de références dans l’objet d’ouverture de session. 
    
   3. Définissez la propriété **PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md)) de l’objet d’état à MAPI_STATUS.
    
   4. Définissez le paramètre de sortie _lppMAPIStatus_ pour pointer vers l’objet de l’état et retourner. 
    
   5. Vérifiez le paramètre d’entrée _ulFlags_ . Si elle est définie à n’et votre fournisseur prend en charge l’accès en lecture/écriture à son objet état, retourne un objet accessible en écriture. Toutefois, si votre fournisseur ne gère pas l’accès en lecture/écriture à son objet état, n’échouent pas. Renvoie un objet état qui est en lecture seule. Les clients qui doivent recevoir les objets d’état en lecture/écriture doivent vérifier que l’autorisation en lecture/écriture a été octroyée avant d’essayer d’apporter des modifications. 
    
2. Définissez toutes les l’état requis d’objet et état de propriétés du tableau. Les propriétés que vous incluez dans votre ligne de tableau d’état doivent être disponibles par le biais de votre objet d’état à l’exception des propriétés calculées par MAPI. Les propriétés requises sont les suivantes :
    
   - **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))
    
   - **PR_PROVIDER_DLL_NAME** ([PidTagProviderDllName](pidtagproviderdllname-canonical-property.md))
    
   - **PR_PROVIDER_DISPLAY** ([PidTagProviderDisplay](pidtagproviderdisplay-canonical-property.md))
    
   - **PR_RESOURCE_TYPE** ([PidTagResourceType](pidtagresourcetype-canonical-property.md))
    
   - **PR_RESOURCE_METHODS** ([PidTagResourceMethods](pidtagresourcemethods-canonical-property.md))
    
   - **PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md))
    
   - **PR_STATUS_CODE** ([PidTagStatusCode](pidtagstatuscode-canonical-property.md))
    
3. Implémenter le [IMAPIStatus : IMAPIProp](imapistatusimapiprop.md) méthodes qui conviennent à votre fournisseur. En fonction de votre fournisseur, il est inutile d’implémenter toutes les quatre méthodes dans **IMAPIStatus**. Chaque fournisseur doit implémenter une version en lecture seule des méthodes de le [IMAPIProp : IUnknown](imapipropiunknown.md) interface et la méthode [IMAPIStatus::ValidateState](imapistatus-validatestate.md) . 

   Fournisseurs de transport doivent également implémenter [IMAPIStatus::FlushQueues](imapistatus-flushqueues.md)et tous les fournisseurs doivent prendre en charge [IMAPIStatus::SettingsDialog](imapistatus-settingsdialog.md). Toutefois, la prise en charge de [IMAPIStatus::ChangePassword](imapistatus-changepassword.md) est facultative. Seuls les fournisseurs de services qui nécessitent des mots de passe et pour permettre aux utilisateurs de les modifier par programme doivent implémenter cette méthode. Pour chaque méthode que vous prenez en charge, définissez le bit correspondant dans la propriété **PR_RESOURCE_METHODS** . Par exemple, si vous prenez en charge **ValidateState** et **dialogue** uniquement, définissez **PR_RESOURCE_METHODS** à ce qui suit : 
    
   `STATUS_VALIDATE_STATE | STATUS_SETTINGS_DIALOG`
    
   Avant d’essayer d’appeler votre objet état, les clients doivent vérifier la valeur de **PR_RESOURCE_METHODS** . Gérer les appels à n’importe lequel de vos méthodes non prises en charge en retournant MAPI_E_NO_SUPPORT. 
    
4. Appelez [IMAPISupport::ModifyStatusRow](imapisupport-modifystatusrow.md) au cours de l’ouverture de session pour ajouter l’ou les lignes à la table d’état. Passez un tableau de valeurs de propriété qui contient les informations de colonne pour la ligne et 0 pour le paramètre _ulFlags_ . Si à un moment donné plus loin dans la session changements d’état de votre fournisseur et qu’il s’avère nécessaire pour mettre à jour les informations de colonne, rappelez **ModifyStatusRow** avec l’indicateur STATUSROW_UPDATE. 
    
Pour plus d’informations sur les objets d’état, voir [Objets d’état MAPI](mapi-status-objects.md).
  
## <a name="see-also"></a>Voir aussi

- [Fournisseurs de services MAPI](mapi-service-providers.md)

