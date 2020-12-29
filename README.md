# Qubes HCL

This repository contains YAML files with data for the [Qubes Hardware Compatibility List](https://www.qubes-os.org/hcl/).

See https://www.qubes-os.org/doc/hcl/ for information on how to submit an HCL report.

## Extra features for hand-written reports

Generally you'll want to follow the above link to submit your report. However, for people who choose to submit their HCL report directly or otherwise hand-modify the YAML, there's an extra feature to be aware of: wherever `yes|no|partial` is accepted, there is a mechanism to override the text that gets displayed. For example, to override the text shown in the TPM column:

```
tpm:
  status: 'yes|no|partial'
  message: 'Text to be displayed goes here'
```

## Template

Template for reports:

```
---
layout:
  'hcl'
type:
  'laptop|desktop|workstation|server|motherboard'
hvm:
  'yes|no|partial'
iommu:
  'yes|no|partial'
tpm:
  'yes|no|partial'
brand: |

model: |

bios: |

cpu: |

cpu-short: |

chipset: |

chipset-short: |

gpu: |

gpu-short: |

network: |

memory: |

scsi: |


versions:

- works:
    'yes|no|partial'
  qubes: |

  xen: |

  kernel: |

  remark: |

  credit: |
    FIXAUTHOR
  link: |
    FIXLINK

---
