---
title: ADRPARM
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ADRPARM
api_type:
- COM
ms.assetid: 35cd57b4-9901-456c-bf06-1f84e274eb4e
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: 560cae5e8a3d73d80a4907fd0fec43b389ef9fc5
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22572024"
---
# <a name="adrparm"></a>ADRPARM

**S’applique à**: Outlook 2013 | Outlook 2016 
  
Décrit l’affichage et le comportement de la boîte de dialogue adresses. 
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapidefs.h  <br/> |
   
```cpp
typedef struct _ADRPARM
{
  ULONG cbABContEntryID;
  LPENTRYID lpABContEntryID;
  ULONG ulFlags;
  LPVOID lpReserved;
  ULONG ulHelpContext;
  LPSTR lpszHelpFileName;
  LPFNABSDI lpfnABSDI;
  LPFNDISMISS lpfnDismiss;
  LPVOID lpvDismissContext;
  LPSTR lpszCaption;
  LPSTR lpszNewEntryTitle;
  LPSTR lpszDestWellsTitle;
  ULONG cDestFields;
  ULONG nDestFieldFocus;
  LPSTR FAR *lppszDestTitles;
  ULONG FAR *lpulDestComps;
  LPSRestriction lpContRestriction;
  LPSRestriction lpHierRestriction;
} ADRPARM, FAR *LPADRPARM;

```

## <a name="members"></a>Members

**cbABContEntryID**
  
> Nombre d’octets de l’identificateur d’entrée désignés par **lpABContEntryID**.
    
**lpABContEntryID**
  
> Pointeur vers l’identificateur d’entrée du conteneur qui fournit la liste initiale des adresses des destinataires qui s’affichent dans la boîte de dialogue.
    
**ulFlags**
  
> Masque de bits d’indicateurs associés à différentes options de la boîte de dialogue adresses. Les indicateurs suivants peuvent être définis :
    
AB_RESOLVE
  
> Activer tous les noms à résoudre après la fermeture de la boîte de dialogue adresses. S’il existe des écritures ambigus qui résultent de la procédure de résolution de nom, une boîte de dialogue s’affiche pour demander à l’utilisateur pour vous aider à résoudre les erreurs. Paramètre de cet indicateur garantit que tous les noms retournés par [IAddrBook::Address](iaddrbook-address.md) sont résolus. 
    
AB_SELECTONLY
  
> Désactiver la création des adresses uniques pour une liste de destinataires. Cet indicateur est utilisé uniquement si la boîte de dialogue est modale, comme indiqué par l’indicateur DIALOG_MODAL en cours.
    
ADDRESS_ONE
  
> L’utilisateur peut sélectionner exactement un destinataire au lieu de plusieurs destinataires à partir d’une liste. Cet indicateur est valide uniquement lorsque **cDestFields** est égale à zéro et la boîte de dialogue est modale, comme indiqué par l’indicateur DIALOG_MODAL en cours. 
    
DIALOG_MODAL
  
> Entraîne la version modale de la boîte de dialogue adresse à afficher. Cet indicateur ou DIALOG_SDI doit être défini ; ils ne peuvent pas être définis. 
    
DIALOG_OPTIONS
  
> Le bouton **Options d’envoi** à afficher dans la boîte de dialogue. Cet indicateur est utilisé uniquement si la boîte de dialogue est modale, comme indiqué par l’indicateur DIALOG_MODAL en cours. 
    
DIALOG_SDI
  
> Entraîne la version non modale de la boîte de dialogue adresse à afficher. Cet indicateur ou DIALOG_MODAL doit être défini ; ils ne peuvent pas être définis. L’indicateur DIALOG_SDI est ignorée pour les clients non Outlook et la version de la boîte de dialogue modale s’affiche. Par conséquent, un pointeur vers un handle ne doit pas dans le paramètre _lpulUIParam_ de [IAddrBook::Address](iaddrbook-address.md).
    
**lpReserved**
  
> Réservé, doit être égal à zéro.
    
**ulHelpContext**
  
> Spécifie le contexte dans l' **aide de** tout d’abord à afficher lorsque l’utilisateur clique sur le bouton Aide dans la boîte de dialogue. 
    
**lpszHelpFileName**
  
> Pointeur vers le nom d’un fichier d’aide qui sera associé à la boîte de dialogue adresses. Le membre **lpszHelpFileName** est utilisé avec **ulHelpContext** pour appeler la fonction Windows **aide Windows** ; 
    
**lpfnABSDI**
  
> Pointeur vers une fonction MAPI basée sur le prototype [ACCELERATEABSDI](accelerateabsdi.md) ou NULL. Ce membre s’applique à la version non modale de la boîte de dialogue, comme indiqué par l’indicateur DIALOG_SDI en cours. Création d’une structure **ADRPARM** à transmettre à [IAddrBook::Address](iaddrbook-address.md) les clients doivent toujours la valeur du membre **lpfnABSDI** NULL. Si l’indicateur DIALOG_SDI est défini, MAPI système puis affectez-lui une fonction valide avant de retourner. Clients appeler cette fonction à partir de leur boucle de message pour vous assurer que les raccourcis dans l’adresse du livre travail boîte de dialogue. Lorsque la boîte de dialogue est fermée et MAPI appelle la fonction vers laquelle pointée le membre **lpfnDismiss** , les clients doivent décrocher la fonction **ACCELERATEABSDI** à partir de leur boucle de message. 
    
**lpfnDismiss**
  
> Pointeur vers une fonction basée sur le prototype [DISMISSMODELESS](dismissmodeless.md) ou NULL. Ce membre s’applique uniquement à la version non modale de la boîte de dialogue, comme indiqué par l’indicateur DIALOG_SDI en cours. MAPI appelle la fonction **DISMISSMODELESS** lorsque l’utilisateur ferme la boîte de dialogue non modale d’adresse pour informer un client appelant **IAddrBook::Address** que la boîte de dialogue n’est plus active. 
    
**lpvDismissContext**
  
> Pointeur vers les informations de contexte à transmettre à la fonction **DISMISSMODELESS** vers laquelle pointée le membre **lpfnDismiss** . Ce membre s’applique uniquement à la version de la boîte de dialogue non modale, telle qu’indiquée par l’indicateur DIALOG_SDI en cours. 
    
**lpszCaption**
  
> Pointeur vers le texte à utiliser comme titre de la boîte de dialogue adresses.
    
**lpszNewEntryTitle**
  
> Pointeur vers le texte à utiliser en tant que l’étiquette du bouton pour le bouton qui appelle la boîte de dialogue **Nouvelle entrée** ou une autre boîte de dialogue. 
    
**lpszDestWellsTitle**
  
> Pointeur vers le texte à utiliser en tant que titre pour les contrôles de zone de texte destinataires qui peuvent apparaître dans la version de la boîte de dialogue adresse modale. Ce membre n’est pas utilisé pour les boîtes de dialogue non modale. 
    
**cDestFields**
  
> Nombre de contrôles de zone de texte destinataire dans la version de la boîte de dialogue adresses, ou zéro si la boîte de dialogue n’est pas modale modale. La boîte de dialogue adresse est ouverte pour la navigation uniquement lorsque les conditions suivantes sont remplies : 
    
  - Le membre **cDestFields** est défini sur zéro. 
    
  - L’indicateur DIALOG_BOX est défini.
    
  - L’indicateur ADDRESS_ONE n’est pas définie.
    
  Définition de **cDestFields** 0xFFFFFFFF implique que MAPI doit créer le nombre de destinataire texte par défaut des contrôles de zone. Dans ce cas, les membres **lppszDestTitles** et **lpulDestComps** doivent être NULL. 
    
**nDestFieldFocus**
  
> Indique le contrôle de zone de texte spécifique qui doit avoir le focus initial lorsque la version de la boîte de dialogue modale s’affiche. Cette valeur doit être comprise entre 0 et la valeur de **cDestFields** moins 1. 
    
**lppszDestTitles**
  
> Pointeur vers un tableau d’étiquettes pour les boutons associés à chacun des contrôles de zone de texte qui sont affichés dans la version de la boîte de dialogue adresse modale. La valeur du membre **cDestFields** indique le nombre d’étiquettes inclus dans le tableau. Si le membre **lppszDestTitles** est NULL, la méthode **adresse** utilise des titres par défaut. 
    
**lpulDestComps**
  
> Pointeur vers un tableau de valeurs de type de destinataire, tel que MAPI_TO, ni et MAPI_BCC, qui est associé à chaque contrôle de zone de texte. La valeur du membre **CDestFields** indique le nombre de types de destinataires inclus dans le tableau. Les valeurs désignés par **lpulDestComps** peuvent être utilisées pour définir la propriété **PR_RECIPIENT_TYPE** ([PidTagRecipientType](pidtagrecipienttype-canonical-property.md)) de chaque destinataire. Si le membre **lpulDestComps** est NULL, la méthode **adresse** utilise les types de destinataires par défaut. 
    
**lpContRestriction**
  
> Pointeur vers une structure [SRestriction](srestriction.md) qui limite le type d’entrées d’adresses qui peut être affiché dans la boîte de dialogue. 
    
**lpHierRestriction**
  
> Pointeur vers une structure **SRestriction** qui limite les conteneurs du carnet d’adresses qui peuvent fournir des entrées d’adresses à afficher dans la boîte de dialogue. 
    
## <a name="remarks"></a>Remarques

Structures **ADRPARM** sont utilisés par les clients et les fournisseurs de services pour contrôler l’apparence et le comportement des boîtes de dialogue courantes adresse MAPI. Il existe deux variantes de la boîte de dialogue adresse : non modal et modal. Certains des membres de la structure **ADRPARM** s’appliquent à ces deux versions de la boîte de dialogue, mais certaines s’appliquent uniquement à un des deux versions. Le tableau suivant concerne les membres d’une structure **ADRPARM** leur utilisation avec les boîtes de dialogue adresse courantes. 
  
|Membre ADRPARM|Type de boîte de dialogue|
|:-----|:-----|
|**cbABContEntryID** et **lpABContEntryID** <br/> |Modales et non modales  <br/> |
|**ulFlags** <br/> |Modales et non modales  <br/> |
|**lpReserved** <br/> |Modales et non modales  <br/> |
|**ulHelpContext** et **lpszHelpFileName** <br/> |Modales et non modales  <br/> |
|**lpfnABSDI** <br/> |Non modal  <br/> |
|**lpfnDismiss** et **lpvDismissContext** <br/> |Non modal  <br/> |
|**lpszCaption** <br/> |Modales et non modales  <br/> |
|**lpszNewEntryTitle** <br/> |Modal  <br/> |
|**lpszDestWellsTitle**, **cDestFields**, **nDestFieldFocus**, **lppszDestTitles**et **lpulDestComps** <br/> |Modal  <br/> |
|**lpContRestriction** <br/> |Modales et non modales  <br/> |
|**lpHierRestriction** <br/> |Modales et non modales  <br/> |
   
La boîte de dialogue non modale est un affichage en lecture seule des entrées à partir d’un ou plusieurs conteneurs de carnet d’adresses. La boîte de dialogue pour afficher toutes les entrées dans les conteneurs sélectionnés ou être limitées aux seuls les entrées et les conteneurs qui correspondent aux critères établis par une restriction. La restriction de contenu vers laquelle pointée **lpContRestriction** peut limiter les types de données saisies et la restriction de hiérarchie désignée par **lpHierRestriction** peut limiter les conteneurs fournissant les entrées. Pour informer l’appelant lorsque la boîte de dialogue est fermée, MAPI appelle une fonction qui est fournie par l’appelant qui établit une correspondance avec le prototype [DISMISSMODELESS](dismissmodeless.md) . Une autre fonction, celle qui correspond le prototype [ACCELERATEABSDI](accelerateabsdi.md) , est fournie par MAPI et appelée par l’appelant dans la boucle de message Windows afin de faciliter l’utilisation des raccourcis clavier. La version de la boîte de dialogue adresse MAPI non modale peut être affichée lorsque les clients appellent [IAddrBook::Address](iaddrbook-address.md) ou [IMAPISupport::Address](imapisupport-address.md)d’appeler les fournisseurs de services. 
  
La boîte de dialogue modale est un affichage en lecture/écriture des entrées à partir d’un ou plusieurs conteneurs. Son contenu peut être affecté de la même manière la version non modale par des restrictions définie dans le **lpContRestriction** et **lpHierRestriction** membres. En plus de la zone de liste affichant les entrées de conteneur, la boîte de dialogue modale peut contenir entre un et trois contrôles de zone de texte pour contenir les entrées sélectionnées par l’utilisateur. Chaque contrôle d’édition est associé à un type de destinataire spécifique ou de la propriété **PR_RECIPIENT_TYPE** tels que MAPI_TO. La boîte de dialogue modale adresse peut être affichée par une des méthodes **adresse** ou lorsque les clients appellent [IAddrBook::Details](iaddrbook-details.md) et fournisseurs de services [IMAPISupport::Details](imapisupport-details.md). 
  
Cette illustration comprend deux contrôles de zone de texte, car le membre **cDestFields** de la structure **ADRPARM** contrôle l’affichage de cette boîte de dialogue est défini sur 2. Le premier contrôle a le focus initial, car le membre **nDestFieldFocus** est défini sur 0. 
  
Le membre **lpszNewEntryTitle** pointe vers le texte d’une étiquette de bouton qui, lorsqu’elle est sélectionnée, affiche une boîte de dialogue supplémentaire s’affiche. En règle générale, comme le montre l’illustration de la boîte de dialogue modale, le bouton est intitulé **New** et la boîte de dialogue qui s’affiche répertorie tous les types d’adresses qui peuvent être créés par des fournisseurs du carnet d’adresses dans le profil. Clients de cette boîte de dialogue **Nouvelle entrée** s’affiche en appelant [IAddrBook::NewEntry](iaddrbook-newentry.md) et en passant de zéro pour le paramètre _cbEidNewEntryTpl_ et NULL pour le paramètre _lpEidNewEntryTpl_ lorsque l’utilisateur sélectionne le bouton Créer. Les informations qui sont incluses dans cette boîte de dialogue proviennent de la table unique MAPI. 
  
Chaque entrée de cette boîte de dialogue est associée à un modèle pour la saisie de données requises pour créer une adresse de type particulier. La plupart des fournisseurs de carnet d’adresses fournissent un modèle pour chaque type d’entrée d’adresse qu’ils peuvent créer. Lorsqu’un utilisateur effectue une sélection à partir de cette boîte de dialogue, MAPI affiche le modèle correspondant.
  
Les quatre bits plus significatives du membre **ulFlags** de la structure **ADRPARM** contiennent un numéro de version qui identifie la version de la structure **ADRPARM** . La version actuelle est 0 (zéro) ou ADRPARM_HELP_CTX. L’implémentation actuelle de MAPI échoue pour n’importe quelle version de la structure de zéro. 
  
Les versions futures de la structure peuvent être totalement différentes ; ils ne peuvent pas en charge la structure de la version de zéro. Les macros suivantes sont fournies pour extraire le numéro de version à partir du membre **ulFlags** et pour combiner avec indicateurs définis : 
  
- **GET_ADRPARM_VERSION** (_ulFlags_) 
- **SET_ADRPARM_VERSION** (_ulFlags_, _ ulVersion _) 
- **ADRPARM_HELP_CTX**
  
## <a name="see-also"></a>Voir aussi

- [ACCELERATEABSDI](accelerateabsdi.md)
- [DISMISSMODELESS](dismissmodeless.md)
- [IAddrBook::Address](iaddrbook-address.md)
- [IMAPISupport::Address](imapisupport-address.md)
- [SRestriction](srestriction.md)
- [Structures MAPI](mapi-structures.md)

