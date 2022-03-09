---
title: Identification de l’historique de téléchargement de message pour un compte POP3
manager: soliver
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: overview
ms.localizationpriority: medium
ms.assetid: 90a51150-5c2c-4d5b-8717-5dacc8532744
description: Cette rubrique décrit comment un client de messagerie peut accéder à la propriété PidTagAttachDataBinary pour obtenir l’historique de téléchargement des messages pour un compte POP3.
ms.openlocfilehash: cb599313b4ec7523a4b6d0ae3775032978115966
ms.sourcegitcommit: 518845d053a009b11c8d907a33822161c0b6bc96
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/08/2022
ms.locfileid: "63374767"
---
# <a name="locating-the-message-download-history-for-a-pop3-account"></a>Identification de l’historique de téléchargement de message pour un compte POP3

Cette rubrique décrit comment un client de messagerie peut accéder à la [propriété PidTagAttachDataBinary](https://msdn.microsoft.com/library/3b0a8b28-863e-4b96-a4c0-fdb8f40555b9%28Office.15%29.aspx) pour obtenir l’historique de téléchargement des messages pour un compte POP3.

<a name="OL15Con_AuxRef_LocatingMsgsUIDLHistory_WhyGetUIDLHistory"> </a>

## <a name="why-get-the-message-download-history"></a>Pourquoi obtenir l’historique de téléchargement des messages ?

Le fournisseur POP (Post Office Protocol) pour Outlook permet aux utilisateurs de récupérer et de télécharger de nouveaux messages électroniques sur leur appareil local, puis de les laisser ou de les supprimer sur le serveur de messagerie. Lorsque le client de messagerie recherche les nouveaux messages à télécharger, il doit être en mesure d’identifier et de télécharger uniquement les nouveaux messages pour cette boîte de réception. Pour ce faire, le client de messagerie utilise d’abord la commande UIDL (Unique ID Listing), qui obtient une carte de chaque message qui a déjà été remis à cette boîte de réception à un identificateur unique (UID). Le client obtient également l’historique de téléchargement des messages pour les messages qui ont été téléchargés ou supprimés pour la boîte de réception sur ce client. À l’aide de la carte UID du message et de l’historique de téléchargement, le client peut ensuite identifier les messages absents dans l’historique comme nouveaux et, par conséquent, doivent être téléchargés.
  
Pour obtenir l’historique de téléchargement des messages pour une boîte de réception :
  
- Suivez les étapes de cette rubrique pour rechercher la propriété **PidTagAttachDataBinary** , qui contient l’historique dans un objet BLOB (Binary Large Object) qui suit un format spécifique.

- Poursuivez avec l’historique de téléchargement des messages pour un compte [POP3](parsing-the-message-download-history-for-a-pop3-account.md), qui décrit comment l’identifier afin d’identifier les messages qui ont été téléchargés ou supprimés pour cette boîte de réception.

## <a name="core-concepts-to-know-for-locating-the-message-download-history"></a>Concepts fondamentaux à connaître pour la localisation de l’historique de téléchargement des messages

L’historique de téléchargement des messages d’une boîte de réception est stocké dans une propriété MAPI binaire, **PidTagAttachDataBinary**, sur une pièce jointe d’un message masqué dans la boîte de réception. Le tableau 1 présente les ressources pour les concepts qui vous aident à comprendre comment localiser l’historique de téléchargement des messages.
  
**Tableau 1. Concepts de base**

|**Titre d’article**|**Description**|
|:-----|:-----|
|[Dossiers masqués MAPI](https://msdn.microsoft.com/library/8b3b9c80-f7f4-4f37-bd6b-323469d020f1%28Office.15%29.aspx) <br/> |MAPI permet aux clients de messagerie de stocker des informations dans des dossiers masqués et des messages masqués. Les dossiers masqués se trouve dans la partie associée des dossiers MAPI et contiennent généralement des informations qui ne sont pas visibles et qui ne doivent pas être manipulées par les utilisateurs. Les clients décident du format et du contenu à stocker dans les messages masqués dans les dossiers masqués. |
|[MAPI Messages](https://msdn.microsoft.com/library/417c113f-bd98-4515-85d1-09db7fc3a227%28Office.15%29.aspx) <br/> |MAPI stocke les messages dans des dossiers, soit dans la sous-arbre IPM standard visible par les utilisateurs d’un client, soit en dehors de la sous-arbre et invisible pour les utilisateurs. Les messages peuvent avoir des données supplémentaires stockées dans une pièce jointe, qui peuvent prendre la forme d’un fichier, d’un autre message ou d’un objet OLE. Dans le cas de l’historique de téléchargement des messages, l’historique est stocké dans une propriété d’un message joint à un autre message masqué. |
|[Vue d’ensemble des propriétés de message](https://msdn.microsoft.com/library/447f54de-9f0d-4f73-89b6-bed9cfea9c15%28Office.15%29.aspx) <br/> |Lorsqu’un client stocke des informations dans un message, il stocke en fait les informations dans une propriété du message. MAPI prend en charge de nombreuses propriétés (certaines existent toujours et peuvent être définies par les clients, d’autres sont facultatives) et les clients ne peuvent pas s’attendre à ce qu’elles soient disponibles ou définies sur des valeurs valides. L’historique de téléchargement des messages est stocké dans la **propriété PidTagAttachDataBinary** d’une pièce jointe à un message masqué. |
|[Profils MAPI](https://msdn.microsoft.com/library/493c87a4-317d-47ec-850b-342cac59594b%28Office.15%29.aspx) <br/> |Au moment de l’ouverture de session, le client de messagerie sélectionne un profil qui décrit les fournisseurs et services à utiliser. Un profil est divisé en sections qui contiennent des propriétés. En particulier, les propriétés [PidTagSearchKey](https://msdn.microsoft.com/library/fcab369a-a1f4-4425-a272-e35046914a4d%28Office.15%29.aspx) (**PR_SEARCH_KEY**) et [PidTagProfileName](https://msdn.microsoft.com/library/13ca726d-ae7a-4da9-9c8e-3db3c479f839%28Office.15%29.aspx) (**PR_PROFILE_NAME**) existent toujours. La clé de recherche d’un profil est unique parmi tous les profils et est stockée dans la section de profil identifiée par **MUID_PROFILE_INSTANCE** (qui est définie dans MAPIGUID. H). Utilisez [IMAPISession::OpenProfileSection](https://msdn.microsoft.com/library/e2757028-27e7-4fc0-9674-e8e30737ef1d%28Office.15%29.aspx) pour ouvrir la section et utilisez [IMAPIProp::GetProps](https://msdn.microsoft.com/library/1c7a9cd2-d765-4218-9aee-52df1a2aae6c%28Office.15%29.aspx) pour obtenir les valeurs de propriété. |
|[Tables des matières](https://msdn.microsoft.com/library/7b8efb4e-b5be-41b8-81bb-9aa1da421433%28Office.15%29.aspx) <br/> |Les fournisseurs de magasins de messages implémentent des tables de contenu pour leurs dossiers. Pour les messages masqués dans la partie associée d’un dossier, les fournisseurs de magasins de messages prendre en charge les tables de contenu associées et les clients peuvent utiliser la méthode [IMAPIContainer::GetContentsTable](https://msdn.microsoft.com/library/88c7a666-875d-473a-b126-dbbb7009f7d9%28Office.15%29.aspx) pour renvoyer un pointeur vers la table des matières associée. |
|[À propos des restrictions](https://msdn.microsoft.com/library/e119fa20-08b8-4c8d-93fc-56037220890d%28Office.15%29.aspx) <br/> [Types de restrictions](https://msdn.microsoft.com/library/0d3bd58b-7100-4117-91ac-27139715c85b%28Office.15%29.aspx) <br/> [Création d’une restriction](https://msdn.microsoft.com/library/12abbd8c-f825-493e-af42-344371d9658e%28Office.15%29.aspx) <br/> [Exemple de code de restriction](https://msdn.microsoft.com/library/9b82097c-dbd6-4ba0-a6cb-292301f9402b%28Office.15%29.aspx) <br/> |Dans MAPI, les clients peuvent utiliser des restrictions pour filtrer les tables de contenu, afin de rechercher des lignes qui représentent des messages dont une propriété spécifique est définie sur une valeur spécifique. Les restrictions sont définies à l’aide de la structure de données [SRestriction](https://msdn.microsoft.com/library/c12b4409-da6f-480b-87af-1e5baea2e8bd%28Office.15%29.aspx) , qui peut contenir une union de structures de restriction plus spécialisées. La [méthode IMAPITable::FindRow](https://msdn.microsoft.com/library/6511368c-9777-497e-9eea-cf390c04b92e%28Office.15%29.aspx) applique une restriction et récupère la première ligne d’un tableau qui correspond aux critères de restriction. |
|[À propos de l’inscription des magasins pour l’indexation](https://msdn.microsoft.com/library/dd2aa06a-96e8-1291-18b5-fc3c40b74e4d%28Office.15%29.aspx) <br/> |Utilisez la [propriété PidTagStoreProvider](https://msdn.microsoft.com/library/6f6cc66f-a08e-4f8e-b33a-d3674319248e%28Office.15%29.aspx) (**PR_MDB_PROVIDER**) pour vérifier le type de fournisseur de magasin. Par exemple, pour vérifier si un magasin est un magasin Exchange, la propriété **PidTagStoreProvider** doit renvoyer une valeur représentée par la constante **pbExchangeProviderPrimaryUserGuid**, qui est définie dans le fichier d’en-tête public edkmdb.h. |

## <a name="locating-the-appropriate-hidden-message-and-attachment"></a>Localisation du message masqué et de la pièce jointe appropriés

Maintenant que nous savons que l’historique de téléchargement des messages pour une boîte de réception se trouve dans la propriété **PidTagAttachDataBinary** d’une pièce jointe à un message masqué, la procédure de localisation de la pièce jointe appropriée du message masqué approprié implique les procédures suivantes :
  
1. [Rechercher le message masqué approprié](#OL15Con_AuxRef_LocatingMsgsUIDLHistory_FindHiddenMsg)

2. [Rechercher la pièce jointe appropriée du message masqué](#OL15Con_AuxRef_LocatingMsgsUIDLHistory_FindAttachment)

3. [Accéder à la propriété PidTagAttachDataBinary de la pièce jointe du message](#OL15Con_AuxRef_LocatingMsgsUIDLHistory_AccessProp)

<a name="OL15Con_AuxRef_LocatingMsgsUIDLHistory_FindHiddenMsg"> </a>

### <a name="find-the-appropriate-hidden-message"></a>Rechercher le message masqué approprié

1. Obtenez la [propriété PidTagSearchKey](https://msdn.microsoft.com/library/fcab369a-a1f4-4425-a272-e35046914a4d%28Office.15%29.aspx) (**PR_SEARCH_KEY**) à partir du profil, dans la section de profil spécifiée par **MUID_PROFILE_INSTANCE**.

2. Ouvrez le contenu associé pour le dossier Boîte de réception en appelant **IMAPIContainer::GetContentsTable**.

3. Créez une restriction basée sur les [propriétés PidTagConversationKey](https://msdn.microsoft.com/library/52c97d6c-7f4b-4522-aeac-0c1ed8475952%28Office.15%29.aspx) (**PR_CONVERSATION_KEY**), **PidTagSearchKey** (**PR_SEARCH_KEY**) et [PidTagMessageClass](https://msdn.microsoft.com/library/1e704023-1992-4b43-857e-0a7da7bc8e87%28Office.15%29.aspx) (**PR_MESSAGE_CLASS**) pour obtenir une table qui contient tous les messages masqués dans le contenu associé de la boîte de réception. Voici un exemple de restriction extraite de [Locating the POP3 UIDL History](https://blogs.msdn.com/b/stephen_griffin/archive/2012/12/03/locating-the-pop3-uidl-history.aspx).

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

4. Dans le tableau, recherchez le message masqué à l’aide **d’IMAPITable::FindRow**.

5. Si l’étape 4 ne trouve pas de message masqué, modifiez la restriction pour utiliser **PidTagSearchKey** (**PR_SEARCH_KEY**) au lieu de **PidTagConversationKey**, comme illustré ci-dessous :

   ```cpp
    rgRes[1].res.resProperty.ulPropTag = rgProps[0].ulPropTag = PR_SEARCH_KEY;
   ```

6. Recherchez le message masqué à **l’aide d’IMAPITable::FindRow**.

7. Si l’étape 6 échoue, modifiez la restriction pour utiliser [PidTagSubject](https://msdn.microsoft.com/library/aa7ba4d9-c5e0-4ce7-a34e-65f675223bc9%28Office.15%29.aspx) (**PR_SUBJECT**) en étant égal à la valeur suivante ( `printf` illustré ci-dessous à l’aide de la substitution de style pour des raisons de concision).

   ```cpp
    "Outlook Message Manager (%s) (KEY: %s)", PR_PROFILE_NAME, HexFromBin(PR_SEARCH_KEY)
   ```

8. Recherchez le message masqué à **l’aide d’IMAPITable::FindRow**.

9. Si vous exécutez Outlook 2010 ou une version ultérieure, utilisez les valeurs suivantes pour **PidTagProfileName** (**PR_PROFILE_NAME**) et **PidTagSearchKey** (**PR_SEARCH_KEY**), respectivement.

   ```cpp
    CHAR g_szGeneralKey[] = "General Key"; 
    const SBinary g_binGeneralKey = {sizeof(g_szGeneralKey), (LPBYTE)g_szGeneralKey};
   ```

   Exécutez les étapes 3 à 8. Si cela ne parvient pas à trouver un message, revenir aux étapes d’origine 3 à 8.

10. Ouvrez le message masqué trouvé à l’étape 4, 6 ou 8.

<a name="OL15Con_AuxRef_LocatingMsgsUIDLHistory_FindAttachment"> </a>

### <a name="find-the-appropriate-attachment-of-the-hidden-message"></a>Rechercher la pièce jointe appropriée du message masqué

Étant donné que le message masqué peut avoir plusieurs pièces jointes, recherchez la pièce jointe appropriée dans l’ordre suivant.
  
> [!NOTE]
> Cette procédure utilise de nouveau la `printf` substitution de style pour des raisons de concision.

1. Recherchez une pièce jointe dont [pidTagAttachLongFilename](https://msdn.microsoft.com/library/83b69e8f-0b5a-4992-b5b8-160d3bdfa22a%28Office.15%29.aspx) (**PR_ATTACH_LONG_FILENAME**) correspond à la chaîne suivante, `szEmailAddress` où se trouve l’adresse SMTP de l’utilisateur, comme spécifié dans le profil de l’utilisateur. .

   ```cpp
    "BlobPOP%s", szEmailAddress
   ```

2. Recherchez une pièce jointe dont [pidTagAttachFilename](https://msdn.microsoft.com/library/cbf34dd6-7733-47f6-9c41-9d82656ca9dc%28Office.15%29.aspx) (**PR_ATTACH_FILENAME**) correspond à « BlobPOP%s ». `szEmailAddress`

3. Recherchez une pièce jointe [dont pidTagDisplayName](https://msdn.microsoft.com/library/bd094e00-5c60-4bb3-9a45-b943fab52876%28Office.15%29.aspx) (**PR_DISPLAY_NAME**) correspond à « BlobPOP%s ». `szEmailAddress`

4. Recherchez une pièce jointe dont **pidTagAttachFilename** (**PR_ATTACH_FILENAME**) correspond à « Blob%.8x `dwAcctUID``dwAcctUID` », où provient [PROP_ACCT_MINI_UID](prop_acct_mini_uid.md). Vous pouvez utiliser la [méthode IOlkAccount::GetProp](iolkaccount-getprop.md) pour accéder à **PROP_ACCT_MINI_UID** propriété.

<a name="OL15Con_AuxRef_LocatingMsgsUIDLHistory_AccessProp"> </a>

### <a name="access-the-pidtagattachdatabinary-property-of-the-message-attachment"></a>Accéder à la propriété PidTagAttachDataBinary de la pièce jointe du message

Après avoir localis la pièce jointe de message appropriée du message masqué, utilisez **IMAPIProp::GetProps** pour lire la propriété **PidTagAttachDataBinary** de la pièce jointe.

<a name="OL15Con_AuxRef_LocatingMsgsUIDLHistory_NextSteps"> </a>

## <a name="next-steps"></a>Étapes suivantes

Vous avez appris à partir de cette rubrique comment localiser l’historique de téléchargement des messages pour la boîte de réception d’un client de messagerie POP3. [Consultez l’historique](parsing-the-message-download-history-for-a-pop3-account.md) de téléchargement des messages pour un compte POP3 pour découvrir comment l’identifier afin d’identifier les messages qui ont été téléchargés ou supprimés pour la boîte de réception.

<a name="OL15Con_AuxRef_LocatingMsgsUIDLHistory_AdditionalRsc"> </a>

## <a name="see-also"></a>Voir aussi

- [Gestion des téléchargements de messages pour les comptes POP3](managing-message-downloads-for-pop3-accounts.md)
- [L'analyse de l'historique de téléchargement des messages pour un compte POP3](parsing-the-message-download-history-for-a-pop3-account.md)
- [Localisation de l’historique UIDL POP3](https://blogs.msdn.com/b/stephen_griffin/archive/2012/12/03/locating-the-pop3-uidl-history.aspx)
