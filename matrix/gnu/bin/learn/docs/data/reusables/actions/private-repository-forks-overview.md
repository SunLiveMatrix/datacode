If you rely on using forks of your private repositories, you can configure policies that control how users can run workflows on `pull_request` events. {% ifversion fpt %}Available to private repositories only, you can configure these policy settings for organizations or repositories.{% else %}Available to private and internal repositories only, you can configure these policy settings for {% ifversion ghec %}enterprises{% else %}your enterprise{% endif %}, organizations, or repositories.{% endif %}