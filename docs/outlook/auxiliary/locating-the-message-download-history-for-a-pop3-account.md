---
title: Localisation de l’historique de téléchargement des messages pour un compte POP3
manager: soliver
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 90a51150-5c2c-4d5b-8717-5dacc8532744
description: Cette rubrique décrit comment un client de messagerie peut accéder à la propriété PidTagAttachDataBinary pour obtenir l’historique de téléchargement des messages pour un compte POP3.
ms.openlocfilehash: 00cf5b02e29a22b5165a4aa339230b604722ab6d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19782740"
---
# <a name="locating-the-message-download-history-for-a-pop3-account"></a>Localisation de l’historique de téléchargement des messages pour un compte POP3

Cette rubrique décrit comment un client de messagerie peut accéder à la propriété [PidTagAttachDataBinary](http://msdn.microsoft.com/library/3b0a8b28-863e-4b96-a4c0-fdb8f40555b9%28Office.15%29.aspx) pour obtenir l’historique de téléchargement des messages pour un compte POP3. 

<a name="OL15Con_AuxRef_LocatingMsgsUIDLHistory_WhyGetUIDLHistory"> </a>

## <a name="why-get-the-message-download-history"></a>Pourquoi obtenir l’historique de téléchargement des messages ?

Le fournisseur Post Office Protocol (POP) pour Outlook permet aux utilisateurs pour récupérer et télécharger les nouveaux messages électroniques sur leur appareil local et ensuite conserver ou supprimer les messages électroniques sur le serveur de messagerie. Lorsque le client de messagerie vérifie les nouveaux messages à télécharger, il doit être en mesure d’identifier et de télécharger uniquement les nouveaux messages pour cette boîte de réception. Pour cela, le client de messagerie premier à l’aide de la commande UIDL (liste des ID uniques), qui obtient un mappage de chaque message qui a déjà été remis à cette boîte de réception à un identificateur unique (UID). Le client obtient également l’historique de téléchargement du message pour les messages qui ont été téléchargés ou supprimés de la boîte de réception sur ce client. À l’aide de la carte UID de message et l’historique de téléchargement, le client peut ensuite identifier les messages qui sont absents dans l’historique en tant que nouvelle et, par conséquent, doit être téléchargé.
  
Pour obtenir l’historique de téléchargement des messages pour une boîte de réception :
  
- Suivez les étapes décrites dans cette rubrique pour trouver la propriété **PidTagAttachDataBinary** , qui contient l’historique dans un objet binaire volumineux (BLOB) qui suit un format spécifique. 
    
- Continuez avec [l’analyse de l’historique de téléchargement des messages pour un compte POP3](parsing-the-message-download-history-for-a-pop3-account.md), qui décrit comment analyser ce BLOB pour identifier les messages qui ont été téléchargés ou supprimés pour cette boîte de réception.
    
## <a name="core-concepts-to-know-for-locating-the-message-download-history"></a>Principaux concepts à connaître pour localiser le message l’historique de téléchargement

L’historique de téléchargement des messages pour une boîte de réception est stocké dans une propriété MAPI binaire, **PidTagAttachDataBinary**, sur une pièce jointe d’un message masqué dans la boîte de réception. Le tableau 1 présente les ressources pour les concepts que vous aident à comprendre comment le message de l’historique de téléchargement.
  
**Le tableau 1. Concepts de base**

|**Titre d’article**|**Description**|
|:-----|:-----|
|[Dossiers MAPI masqué](http://msdn.microsoft.com/library/8b3b9c80-f7f4-4f37-bd6b-323469d020f1%28Office.15%29.aspx) <br/> |MAPI permet aux clients de messagerie stocker les informations dans des dossiers cachés et messages masqués. Dossiers cachés se trouvent dans la partie associée de dossiers MAPI et contient généralement des informations ne sont pas visibles à et de ne pas être manipulées par les utilisateurs. Clients de choisir le format et le contenu à stocker dans les messages masqués dans des dossiers cachés.  <br/> |
|[Messages MAPI](http://msdn.microsoft.com/library/417c113f-bd98-4515-85d1-09db7fc3a227%28Office.15%29.aspx) <br/> |MAPI stocke les messages dans les dossiers, dans la sous-arborescence IPM standard qui est visible pour les utilisateurs d’un client, ou en dehors de la sous-arborescence et invisible aux utilisateurs. Les messages peuvent avoir des données supplémentaires stockées dans une pièce jointe, qui peut être sous la forme d’un fichier, un autre message ou un objet OLE. Dans le cas de l’historique de téléchargement de message, l’historique est stocké dans une propriété d’un message qui est attaché à un autre message masqué.  <br/> |
|[Vue d’ensemble des propriétés de message](http://msdn.microsoft.com/library/447f54de-9f0d-4f73-89b6-bed9cfea9c15%28Office.15%29.aspx) <br/> |Lorsqu’un client stocke des informations dans un message, il stocke réellement les informations dans une propriété du message. MAPI prend en charge de nombreuses propriétés — certains toujours existent peuvent être définies par les clients et d’autres sont facultatifs, et les clients ne peuvent pas qu’ils doivent être disponibles ou défini à des valeurs valides. L’historique de téléchargement du message est stocké dans la propriété **PidTagAttachDataBinary** d’une pièce jointe à un message masqué.  <br/> |
|[Profils MAPI](http://msdn.microsoft.com/library/493c87a4-317d-47ec-850b-342cac59594b%28Office.15%29.aspx) <br/> |Au moment de l’ouverture de session dans une session, le client de messagerie sélectionne un profil qui décrit les fournisseurs et les services à utiliser. Un profil est divisé en sections qui contiennent des propriétés. En particulier, le [PidTagSearchKey](http://msdn.microsoft.com/library/fcab369a-a1f4-4425-a272-e35046914a4d%28Office.15%29.aspx) (**clé PR_SEARCH_KEY**) et [PidTagProfileName](http://msdn.microsoft.com/library/13ca726d-ae7a-4da9-9c8e-3db3c479f839%28Office.15%29.aspx) (**PR_PROFILE_NAME**) Propriétés toujours existent. Clé de recherche d’un profil est unique parmi tous les profils et est stockée dans la section profil identifié par **MUID_PROFILE_INSTANCE** (qui est défini dans MAPIGUID. H). Utilisez [IMAPISession::OpenProfileSection](http://msdn.microsoft.com/library/e2757028-27e7-4fc0-9674-e8e30737ef1d%28Office.15%29.aspx) pour ouvrir la section et [IMAPIProp::GetProps](http://msdn.microsoft.com/library/1c7a9cd2-d765-4218-9aee-52df1a2aae6c%28Office.15%29.aspx) pour obtenir les valeurs de propriété.  <br/> |
|[Tables des matières](http://msdn.microsoft.com/library/7b8efb4e-b5be-41b8-81bb-9aa1da421433%28Office.15%29.aspx) <br/> |Tables de contenu pour leurs dossiers implémentés par les fournisseurs de banque de message. Pour les messages masqués dans le composant associé d’un dossier, fournisseurs de banque de messages prennent en charge les tables de contenu associé et clients peuvent utiliser la méthode [IMAPIContainer::GetContentsTable](http://msdn.microsoft.com/library/88c7a666-875d-473a-b126-dbbb7009f7d9%28Office.15%29.aspx) pour renvoyer un pointeur vers le tableau de contenu associée.  <br/> |
|[À propos des Restrictions](http://msdn.microsoft.com/library/e119fa20-08b8-4c8d-93fc-56037220890d%28Office.15%29.aspx) <br/> [Types de Restrictions](http://msdn.microsoft.com/library/0d3bd58b-7100-4117-91ac-27139715c85b%28Office.15%29.aspx) <br/> [Création d’une Restriction](http://msdn.microsoft.com/library/12abbd8c-f825-493e-af42-344371d9658e%28Office.15%29.aspx) <br/> [Exemple de Code de Restriction](http://msdn.microsoft.com/library/9b82097c-dbd6-4ba0-a6cb-292301f9402b%28Office.15%29.aspx) <br/> |MAPI, les clients peuvent utiliser des restrictions pour filtrer les tables des matières, pour rechercher des lignes qui représentent les messages dont une propriété donnée est défini sur une valeur spécifique. Restrictions sont définies à l’aide de la structure de données [SRestriction](http://msdn.microsoft.com/library/c12b4409-da6f-480b-87af-1e5baea2e8bd%28Office.15%29.aspx) , qui peut contenir une union des structures de restriction plus spécialisés. La méthode [IMAPITable::FindRow](http://msdn.microsoft.com/library/6511368c-9777-497e-9eea-cf390c04b92e%28Office.15%29.aspx) applique une restriction et récupère la première ligne dans une table qui correspond aux critères de restriction.  <br/> |
|[Sur l’inscription des magasins pour l’indexation](http://msdn.microsoft.com/library/dd2aa06a-96e8-1291-18b5-fc3c40b74e4d%28Office.15%29.aspx) <br/> |Utilisez la propriété [PidTagStoreProvider](http://msdn.microsoft.com/library/6f6cc66f-a08e-4f8e-b33a-d3674319248e%28Office.15%29.aspx) (**PR_MDB_PROVIDER**) pour vérifier le type de fournisseur de magasins. Par exemple, pour vérifier si un objet store est une banque Exchange, la propriété **PidTagStoreProvider** doit renvoyer une valeur représentée par la constante **pbExchangeProviderPrimaryUserGuid**, qui est définie dans le edkmdb.h de fichier d’en-tête public.  <br/> |
   
## <a name="locating-the-appropriate-hidden-message-and-attachment"></a>Recherche le message masqué approprié et pièces jointes

Maintenant que nous savons que l’historique de téléchargement des messages pour une boîte de réception est dans la propriété **PidTagAttachDataBinary** d’une pièce jointe à un message masqué, la procédure pour localiser la pièce jointe appropriée du message masqué appropriée implique les éléments suivants procédures : 
  
1. [Recherchez le message masqué approprié](#OL15Con_AuxRef_LocatingMsgsUIDLHistory_FindHiddenMsg)
    
2. [Trouver la pièce jointe appropriée du message masqué](#OL15Con_AuxRef_LocatingMsgsUIDLHistory_FindAttachment)
    
3. [Accéder à la propriété PidTagAttachDataBinary de la pièce jointe du message](#OL15Con_AuxRef_LocatingMsgsUIDLHistory_AccessProp)

<a name="OL15Con_AuxRef_LocatingMsgsUIDLHistory_FindHiddenMsg"> </a>

### <a name="find-the-appropriate-hidden-message"></a>Recherchez le message masqué approprié

1. Pour obtenir la propriété [PidTagSearchKey](http://msdn.microsoft.com/library/fcab369a-a1f4-4425-a272-e35046914a4d%28Office.15%29.aspx) (**clé PR_SEARCH_KEY**) à partir du profil, dans la section profil spécifiée par **MUID_PROFILE_INSTANCE**.
    
2. Ouvrir le contenu associé pour le dossier boîte de réception en appelant **IMAPIContainer::GetContentsTable**.
    
3. Créer une restriction selon la [PidTagConversationKey](http://msdn.microsoft.com/library/52c97d6c-7f4b-4522-aeac-0c1ed8475952%28Office.15%29.aspx) (**PR_CONVERSATION_KEY**), **PidTagSearchKey** (**clé PR_SEARCH_KEY**) et les propriétés [PidTagMessageClass](http://msdn.microsoft.com/library/1e704023-1992-4b43-857e-0a7da7bc8e87%28Office.15%29.aspx) (**PR_MESSAGE_CLASS**) pour obtenir un tableau qui contient tous les messages masqués dans le contenu de la boîte de réception associé. Voici un exemple d’une restriction extraite de [localisation de l’historique de UIDL POP3](http://blogs.msdn.com/b/stephen_griffin/archive/2012/12/03/locating-the-pop3-uidl-history.aspx).
    
   ```cpp
      SRestriction rgRes[3]; 
      SPropValue rgProps[3]; 
      rgRes[0].rt = RES_AND; 
      rgRes[0].res.resAnd.cRes = 2; 
      rgRes[0].res.resAnd.lpRes = &amp;rgRes[1]; 
      rgRes[1].rt = RES_PROPERTY; 
      rgRes[1].res.resProperty.relop = RELOP_EQ; 
      rgRes[1].res.resProperty.ulPropTag = PR_CONVERSATION_KEY; 
      rgRes[1].res.resProperty.lpProp = &amp;rgProps[0]; 
      rgRes[2].rt = RES_PROPERTY; 
      rgRes[2].res.resProperty.relop = RELOP_EQ; 
      rgRes[2].res.resProperty.ulPropTag = PR_MESSAGE_CLASS; 
      rgRes[2].res.resProperty.lpProp = &amp;rgProps[1]; 
      rgProps[0].ulPropTag = PR_CONVERSATION_KEY; 
      rgProps[0].Value.bin = pVals[iSearchKey].Value.bin; // PR_SEARCH_KEY from the profile 
      rgProps[1].ulPropTag = PR_MESSAGE_CLASS; 
      rgProps[1].Value.LPSZ = (LPTSTR)"IPM.MessageManager";
   ```

4. Dans le tableau, recherchez le message masqué à l’aide de **IMAPITable::FindRow**.
    
5. Si l’étape 4 ne parvient pas à trouver un message masqué, modifiez la restriction afin d’utiliser **PidTagSearchKey** (**clé PR_SEARCH_KEY**) au lieu de **PidTagConversationKey**, comme illustré ci-dessous :
    
   ```cpp
    rgRes[1].res.resProperty.ulPropTag = rgProps[0].ulPropTag = PR_SEARCH_KEY;
   ```

6. Recherchez le message masqué à l’aide de **IMAPITable::FindRow**. 
    
7. En cas d’échec de l’étape 6, modifiez la restriction pour utiliser [PidTagSubject](http://msdn.microsoft.com/library/aa7ba4d9-c5e0-4ce7-a34e-65f675223bc9%28Office.15%29.aspx) (**PR_SUBJECT**) est égal à la valeur suivante (ci-dessous à l’aide de `printf` style substitution par souci de concision). 
    
   ```cpp
    "Outlook Message Manager (%s) (KEY: %s)", PR_PROFILE_NAME, HexFromBin(PR_SEARCH_KEY)
   ```

8. Recherchez le message masqué à l’aide de **IMAPITable::FindRow**.
    
9. Si vous exécutez Outlook 2010 ou une version ultérieure, utilisez les valeurs suivantes pour **PidTagProfileName** (**PR_PROFILE_NAME**) et **PidTagSearchKey** (**clé PR_SEARCH_KEY**), respectivement.
    
   ```cpp
    CHAR g_szGeneralKey[] = "General Key"; 
    const SBinary g_binGeneralKey = {sizeof(g_szGeneralKey), (LPBYTE)g_szGeneralKey};
   ```

   Exécutez les étapes 3 à 8. Si cette opération échoue rechercher un message, revenir aux étapes 3 à 8 d’origine.
    
10. Ouvrez le message masqué trouvé à l’étape 4, 6 ou 8.

<a name="OL15Con_AuxRef_LocatingMsgsUIDLHistory_FindAttachment"> </a>

### <a name="find-the-appropriate-attachment-of-the-hidden-message"></a>Trouver la pièce jointe appropriée du message masqué

Étant donné que le message masqué peut avoir plusieurs pièces jointes, recherchez la pièce jointe appropriée dans l’ordre suivant.
  
> [!NOTE]
> Cette procédure utilise de nouveau la `printf` style substitution par souci de concision. 

1. Recherchez une pièce jointe dont [PidTagAttachLongFilename](http://msdn.microsoft.com/library/83b69e8f-0b5a-4992-b5b8-160d3bdfa22a%28Office.15%29.aspx) (**PR_ATTACH_LONG_FILENAME**) correspond à la chaîne suivante, où `szEmailAddress` est l’adresse SMTP de l’utilisateur, tel que spécifié dans le profil utilisateur. . 
    
   ```cpp
    "BlobPOP%s", szEmailAddress
   ```

2. Recherchez une pièce jointe dont [PidTagAttachFilename](http://msdn.microsoft.com/library/cbf34dd6-7733-47f6-9c41-9d82656ca9dc%28Office.15%29.aspx) (**PR_ATTACH_FILENAME**) correspond à « BlobPOP %s », `szEmailAddress`.
    
3. Recherchez une pièce jointe dont [PidTagDisplayName](http://msdn.microsoft.com/library/bd094e00-5c60-4bb3-9a45-b943fab52876%28Office.15%29.aspx) (**PR_DISPLAY_NAME**) correspond à « BlobPOP %s », `szEmailAddress`.
    
4. Recherchez une pièce jointe dont **PidTagAttachFilename** (**PR_ATTACH_FILENAME**) correspond à « Blob%.8x », `dwAcctUID`, où `dwAcctUID` provient de [PROP_ACCT_MINI_UID](prop_acct_mini_uid.md). Vous pouvez utiliser la méthode [IOlkAccount::GetProp](iolkaccount-getprop.md) pour accéder à la propriété **PROP_ACCT_MINI_UID** . 

<a name="OL15Con_AuxRef_LocatingMsgsUIDLHistory_AccessProp"> </a>

### <a name="access-the-pidtagattachdatabinary-property-of-the-message-attachment"></a>Accéder à la propriété PidTagAttachDataBinary de la pièce jointe du message

Après avoir localisé la pièce jointe de message approprié du message masqué, utilisez **IMAPIProp::GetProps** pour lire la propriété **PidTagAttachDataBinary** de la pièce jointe. 

<a name="OL15Con_AuxRef_LocatingMsgsUIDLHistory_NextSteps"> </a>

## <a name="next-steps"></a>Étapes suivantes

Vous avez appris à partir de cette rubrique Rechercher l’historique de téléchargement des messages de la boîte de réception d’un client de messagerie POP3. Voir [l’analyse de l’historique de téléchargement des messages pour un compte POP3](parsing-the-message-download-history-for-a-pop3-account.md) pour découvrir comment analyser cet historique pour identifier les messages qui ont été téléchargés ou supprimés de la boîte de réception. 

<a name="OL15Con_AuxRef_LocatingMsgsUIDLHistory_AdditionalRsc"> </a>

## <a name="see-also"></a>Voir aussi

- [Message de la gestion des téléchargements pour les comptes POP3](managing-message-downloads-for-pop3-accounts.md)   
- [L'analyse de l'historique de téléchargement des messages pour un compte POP3](parsing-the-message-download-history-for-a-pop3-account.md)
- [Localisation de l’historique UIDL POP3](http://blogs.msdn.com/b/stephen_griffin/archive/2012/12/03/locating-the-pop3-uidl-history.aspx)
    

